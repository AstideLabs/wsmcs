<script setup lang="ts">
import { computed } from 'vue'

const props = withDefaults(defineProps<{
  variant?: 'primary' | 'secondary'
  href?: string
}>(), {
  variant: 'primary'
})

const buttonClasses = computed(() => {
  const base = "h-[46px] px-5 py-3 rounded-[10px] flex items-center justify-center font-medium text-[16px] leading-normal whitespace-nowrap transition-colors"
  if (props.variant === 'secondary') {
    return `${base} bg-white/60 text-brand-light hover:bg-white/80`
  }
  return `${base} bg-brand-light text-white hover:bg-brand-dark`
})
</script>

<template>
  <component 
    :is="href ? 'a' : 'button'" 
    :href="href"
    :class="buttonClasses"
  >
    <slot />
  </component>
</template>
