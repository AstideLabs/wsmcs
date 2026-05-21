<script setup lang="ts">
import logoImg from '../../assets/images/logo.png'

const navLinks = [
  { name: '首页', href: '#', active: true },
  { name: '文档', href: '#', active: false },
  { name: '实时地图', href: '#', active: false },
]
</script>

<template>
  <header class="fixed top-0 left-0 right-0 z-50 h-[70px] px-4 md:px-11 py-3 bg-white/90 backdrop-blur-[13.6px] flex items-center justify-between pointer-events-auto">
    <!-- Logo -->
    <div class="h-[45px] w-[45px] shrink-0 mix-blend-multiply relative">
      <img :src="logoImg" alt="Logo" class="w-full h-full object-cover" />
    </div>

    <!-- Navigation -->
    <nav class="flex items-center justify-end flex-wrap gap-2 md:gap-5 h-auto md:h-[27px] min-w-0">
      <a 
        v-for="link in navLinks" 
        :key="link.name"
        :href="link.href"
        class="text-[14px] md:text-[15px] font-medium leading-normal truncate"
        :class="link.active ? 'text-brand-dark' : 'text-text-main hover:text-brand transition-colors'"
      >
        {{ link.name }}
      </a>
    </nav>
  </header>
</template>
