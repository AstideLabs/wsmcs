<script setup lang="ts">
import logoImg from '../../assets/images/logo.png'
import social1 from '../../assets/images/social-1.png'
import social2 from '../../assets/images/social-2.png'
import social3 from '../../assets/images/social-3.png'

const socialIcons = [
  { img: social1, link: "#" },
  { img: social2, link: "#" },
  { img: social3, link: "#" }
]
</script>

<template>
  <footer class="bg-bg-gray overflow-hidden relative pb-10">
    <div class="max-w-[1440px] mx-auto w-full relative h-[302px]">
      
      <!-- Logo Info -->
      <div class="absolute left-[62px] top-[55px] flex flex-col items-start">
        <div class="w-[45px] h-[45px] mix-blend-multiply mb-2.5">
          <img :src="logoImg" alt="Logo" class="w-full h-full object-cover" />
        </div>
        <p class="text-[20px] font-semibold text-[#0a75c8] whitespace-nowrap mb-[13px]">
          繁星之望服务器
        </p>
        <div class="text-[14px] font-medium text-text-muted leading-normal">
          <p>一个拥有诸多优点的 Minecraft 高性能养老服务器</p>
          <p>时刻欢迎广大玩家加入。</p>
        </div>
      </div>

      <!-- Links Grid -->
      <div class="absolute top-[30px] right-[80px] flex gap-[95px]">
        <!-- Service -->
        <div class="flex flex-col gap-6 text-[16px] font-medium items-start w-[187px]">
          <h3 class="text-black leading-snug">服务</h3>
          <a href="https://wsmcs.vercel.app/service-center.html" target="_blank" class="text-[#454545] hover:text-brand transition-colors leading-snug">服务中心</a>
          <a href="https://status.wsmcs.top/" target="_blank" class="text-[#454545] hover:text-brand transition-colors leading-snug">服务状态</a>
        </div>
        
        <!-- Docs -->
        <div class="flex flex-col gap-6 text-[16px] font-medium items-start w-[187px]">
          <h3 class="text-black leading-snug">文档</h3>
          <a href="#" class="text-[#454545] hover:text-brand transition-colors leading-snug">帮助文档</a>
          <a href="#" class="text-[#454545] hover:text-brand transition-colors leading-snug">服务条款</a>
          <a href="#" class="text-[#454545] hover:text-brand transition-colors leading-snug">隐私政策</a>
        </div>
        
        <!-- Links -->
        <div class="flex flex-col gap-6 text-[16px] font-medium items-start w-[187px]">
          <h3 class="text-black leading-snug">友情链接</h3>
          <a href="#" class="text-[#454545] hover:text-brand transition-colors leading-snug">ATCraftMC</a>
          <a href="#" class="text-[#454545] hover:text-brand transition-colors leading-snug">ATNetwork</a>
        </div>
      </div>

      <!-- Bottom Bar -->
      <div class="absolute bottom-[18px] left-[62px] right-[56px] flex justify-between items-center h-[40px]">
        <div class="text-[13px] font-medium text-black">
          © 2025 WSMCS, Inc.
        </div>
        <div class="flex items-center gap-2">
          <a v-for="(icon, idx) in socialIcons" :key="idx" :href="icon.link" class="w-10 h-10 rounded-[4px] flex items-center justify-center hover:bg-gray-200 transition-colors">
            <img :src="icon.img" alt="Social" class="w-6 h-6 object-contain" />
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>
