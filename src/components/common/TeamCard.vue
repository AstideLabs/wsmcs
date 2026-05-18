<script setup lang="ts">
export interface Tag {
  label: string
  // If multiple tags are present, they are positioned. We'll handle a simple list.
}

defineProps<{
  name: string
  description: string
  avatarSrc: string
  tags: Tag[]
}>()
</script>

<template>
  <div class="bg-card-gray rounded-[10px] h-[126px] relative shrink-0 w-full drop-shadow-[0_6px_9px_rgba(0,0,0,0.04)]">
    
    <!-- Avatar -->
    <div class="absolute left-[22px] top-[20px] w-[80.4px] h-[80.4px] rounded-full overflow-hidden">
      <img :src="avatarSrc" :alt="name" class="w-full h-full object-cover" />
    </div>

    <!-- Tags -->
    <!-- The tags overlay on the avatar bottom right in the design. We will approximate their position relative to the avatar -->
    <div class="absolute left-[72px] top-[63px] flex flex-col gap-1 z-10">
      <!-- We render them stacked upwards based on the design which sometimes has two tags (e.g. 资金支持 on top of 创始人) -->
      <div 
        v-for="(tag, index) in tags" 
        :key="index"
        class="bg-brand text-white text-[8px] md:text-[10px] font-semibold px-2 py-0.5 rounded-[4px] whitespace-nowrap text-center transform shadow-sm"
        :style="{ marginTop: index > 0 ? '4px' : '0' }"
      >
        {{ tag.label }}
      </div>
    </div>

    <!-- Text Content -->
    <div class="absolute left-[134px] top-[36px] flex flex-col justify-center gap-1.5">
      <h4 class="font-semibold text-black text-[20px] leading-[1.5] whitespace-nowrap">
        {{ name }}
      </h4>
      <p class="font-medium text-black text-[16px] leading-[1.5]">
        {{ description }}
      </p>
    </div>
    
  </div>
</template>
