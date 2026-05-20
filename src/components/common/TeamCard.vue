<script setup lang="ts">
export interface Tag {
  label: string
}

defineProps<{
  name: string
  description: string
  avatarSrc: string
  tags: Tag[]
}>()
</script>

<template>
  <div class="bg-card-gray rounded-[10px] h-auto min-h-[126px] py-[20px] px-[22px] flex items-center gap-[32px] shrink-0 w-full drop-shadow-[0_6px_9px_rgba(0,0,0,0.04)]">
    
    <!-- Avatar Group -->
    <div class="relative shrink-0 w-[80.4px] h-[80.4px]">
      <!-- Avatar Image -->
      <div class="w-full h-full rounded-full overflow-hidden">
        <img :src="avatarSrc" :alt="name" class="w-full h-full object-cover" />
      </div>
      
      <!-- Tags -->
      <div class="absolute -right-2 -bottom-2 flex flex-col gap-1 z-10 items-center">
        <div 
          v-for="(tag, index) in tags" 
          :key="index"
          class="bg-brand text-white text-[8px] md:text-[10px] font-semibold px-2 py-0.5 rounded-[4px] whitespace-nowrap text-center shadow-sm"
        >
          {{ tag.label }}
        </div>
      </div>
    </div>

    <!-- Text Content -->
    <div class="flex flex-col justify-center gap-1.5 min-w-0 flex-1">
      <h4 class="font-semibold text-black text-[18px] md:text-[20px] leading-[1.5] truncate">
        {{ name }}
      </h4>
      <p class="font-medium text-black text-[14px] md:text-[16px] leading-[1.5] line-clamp-2">
        {{ description }}
      </p>
    </div>
    
  </div>
</template>
