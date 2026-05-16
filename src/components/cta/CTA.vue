<script setup lang="ts">
import { ref } from 'vue';

const serverIP = 'play.wsmcs.net'; // Placeholder IP
const copied = ref(false);

const copyIP = async () => {
  try {
    await navigator.clipboard.writeText(serverIP);
    copied.value = true;
    setTimeout(() => {
      copied.value = false;
    }, 2000);
  } catch (err) {
    console.error('Failed to copy text: ', err);
  }
};
</script>

<template>
  <section id="join" class="py-24 relative overflow-hidden">
    <!-- Background -->
    <div class="absolute inset-0 bg-primary z-0"></div>
    <!-- Decorative patterns (optional, kept simple for modern look) -->
    <div class="absolute top-0 left-0 w-full h-full overflow-hidden opacity-10 z-0">
      <div class="absolute -top-[50%] -left-[10%] w-[70%] h-[200%] bg-white rounded-full blur-3xl transform rotate-12"></div>
      <div class="absolute -bottom-[50%] -right-[10%] w-[70%] h-[200%] bg-black rounded-full blur-3xl transform -rotate-12"></div>
    </div>

    <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10 text-center">
      <h2 class="text-3xl md:text-5xl font-extrabold text-white tracking-tight mb-6">
        准备好开始冒险了吗？
      </h2>
      <p class="text-xl text-primary-100 mb-10 max-w-2xl mx-auto font-medium text-blue-100">
        加入数千名玩家的行列，在 WSMCS 创造属于你的传奇故事。支持 Java 版 1.20+
      </p>
      
      <div class="bg-white/10 backdrop-blur-md rounded-3xl p-2 sm:p-4 inline-flex flex-col sm:flex-row items-center gap-4 border border-white/20 shadow-2xl">
        <div class="px-6 py-4 bg-white/10 rounded-2xl">
          <span class="text-2xl font-mono font-bold text-white tracking-wider">{{ serverIP }}</span>
        </div>
        <button 
          @click="copyIP"
          class="w-full sm:w-auto px-8 py-4 bg-white text-primary text-lg font-bold rounded-2xl hover:bg-slate-50 transition-all duration-300 shadow-lg flex items-center justify-center gap-2"
        >
          <svg v-if="!copied" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"></path>
          </svg>
          <svg v-else class="w-6 h-6 text-green-500" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
          </svg>
          {{ copied ? '已复制 IP' : '复制服务器 IP' }}
        </button>
      </div>
    </div>
  </section>
</template>
