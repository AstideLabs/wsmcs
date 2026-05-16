<script setup lang="ts">
</script>

<template>
  <section class="relative min-h-[90vh] flex items-center justify-center pt-20 overflow-hidden">
    <!-- Background Image -->
    <div class="absolute inset-0 z-0">
      <img 
        src="/images/hero-bg.webp" 
        alt="WSMCS Minecraft Server" 
        class="w-full h-full object-cover object-center"
      />
      <!-- Overlay -->
      <div class="absolute inset-0 bg-gradient-to-b from-slate-900/60 via-slate-900/40 to-slate-900/80"></div>
    </div>

    <!-- Content -->
    <div class="relative z-10 text-center px-4 sm:px-6 lg:px-8 max-w-5xl mx-auto">
      <h1 class="text-4xl sm:text-5xl md:text-6xl font-extrabold text-white tracking-tight mb-6 drop-shadow-lg">
        探索无尽的 <span class="text-primary-light">Minecraft</span> 世界
      </h1>
      <p class="mt-4 text-xl sm:text-2xl text-slate-200 max-w-3xl mx-auto mb-10 drop-shadow-md font-medium">
        纯净生存、粘液科技、起床战争，为你打造最极致的游戏体验。立即加入 WSMCS，开启你的冒险之旅！
      </p>
      
      <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
        <a 
          href="#join" 
          class="px-8 py-4 bg-primary text-white text-lg font-bold rounded-full hover:bg-primary-dark transition-all duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-1"
        >
          立即加入服务器
        </a>
        <a 
          href="#features" 
          class="px-8 py-4 bg-white/10 backdrop-blur-md text-white text-lg font-bold rounded-full hover:bg-white/20 transition-all duration-300 border border-white/20 shadow-lg"
        >
          了解特色玩法
        </a>
      </div>
    </div>
  </section>
</template>
