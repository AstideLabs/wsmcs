<script setup lang="ts">
defineProps<{
  title: string
  description: string
  imageSrc: string
}>()
</script>

<template>
  <div class="relative shrink-0 w-full h-[486px] rounded-[24px] overflow-hidden border border-black/10 shadow-[0_6px_18px_rgba(0,0,0,0.04)] group">
    <!-- Background Image & Gradient -->
    <div class="absolute inset-0 pointer-events-none">
      <img :src="imageSrc" alt="" class="absolute w-full h-full object-cover" />
      <div class="absolute inset-0 bg-gradient-to-t from-black/60 via-black/30 to-transparent"></div>
    </div>
    
    <!-- Content -->
    <div class="absolute left-8 bottom-8 flex flex-col gap-1.5 w-[calc(100%-64px)] max-w-[229px] z-10">
      <h3 class="font-semibold text-white text-[24px] leading-[30px] break-words">
        {{ title }}
      </h3>
      <p class="font-medium text-white/90 text-[14px] leading-[18px]">
        {{ description }}
      </p>
    </div>
  </div>
</template>
