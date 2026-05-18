<script setup lang="ts">
defineProps<{
  title: string
  description: string
}>()
</script>

<template>
  <div class="flex flex-col gap-[14px] items-start w-full max-w-[883px] mb-[21px]">
    <h2 class="font-semibold text-brand text-[36px] leading-[1.5]">
      {{ title }}
    </h2>
    <p class="font-normal text-black text-[20px] leading-[1.5] w-full max-w-[1205px]">
      {{ description }}
    </p>
  </div>
</template>
