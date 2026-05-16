<script setup lang="ts">
import { ref } from 'vue';

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<template>
  <nav class="fixed top-0 left-0 right-0 z-50 bg-white/80 backdrop-blur-md border-b border-slate-200">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-20">
        <!-- Logo -->
        <div class="flex-shrink-0 flex items-center gap-3">
          <img src="/images/wsmcs-logo.webp" alt="WSMCS Logo" class="h-10 w-auto" />
          <span class="font-bold text-xl text-slate-800">WSMCS</span>
        </div>

        <!-- Desktop Menu -->
        <div class="hidden md:flex items-center space-x-8">
          <a href="#" class="text-slate-600 hover:text-primary transition-colors duration-200">首页</a>
          <a href="#features" class="text-slate-600 hover:text-primary transition-colors duration-200">特色玩法</a>
          <a href="#staff" class="text-slate-600 hover:text-primary transition-colors duration-200">管理团队</a>
          <a href="#join" class="px-6 py-2.5 bg-primary text-white rounded-full hover:bg-primary-dark transition-all duration-300 shadow-sm hover:shadow-md">加入我们</a>
        </div>

        <!-- Mobile Menu Button -->
        <div class="md:hidden flex items-center">
          <button @click="toggleMenu" class="text-slate-600 hover:text-primary focus:outline-none">
            <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path v-if="!isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
              <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div v-show="isMenuOpen" class="md:hidden bg-white border-b border-slate-200">
      <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
        <a href="#" class="block px-3 py-2 text-base font-medium text-slate-700 hover:text-primary hover:bg-slate-50 rounded-md">首页</a>
        <a href="#features" class="block px-3 py-2 text-base font-medium text-slate-700 hover:text-primary hover:bg-slate-50 rounded-md">特色玩法</a>
        <a href="#staff" class="block px-3 py-2 text-base font-medium text-slate-700 hover:text-primary hover:bg-slate-50 rounded-md">管理团队</a>
        <a href="#join" class="block px-3 py-2 text-base font-medium text-primary hover:text-primary-dark hover:bg-slate-50 rounded-md">加入我们</a>
      </div>
    </div>
  </nav>
</template>
