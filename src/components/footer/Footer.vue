<script setup lang="ts">
const currentYear = new Date().getFullYear();
</script>

<template>
  <footer class="bg-slate-900 pt-16 pb-8 text-slate-300 border-t border-slate-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-12 mb-12">
        <!-- Brand -->
        <div class="col-span-1 md:col-span-1">
          <div class="flex items-center gap-3 mb-6">
            <img src="/images/wsmcs-logo.webp" alt="WSMCS Logo" class="h-10 w-auto opacity-90" />
            <span class="font-bold text-xl text-white">WSMCS</span>
          </div>
          <p class="text-slate-400 mb-6 max-w-sm">
            一个致力于为玩家提供最优质 Minecraft 体验的社区服务器。纯净生存，粘液科技，起床战争，尽在这里。
          </p>
        </div>

        <!-- Links -->
        <div>
          <h3 class="text-lg font-bold text-white mb-6">快速链接</h3>
          <ul class="space-y-4">
            <li><a href="#" class="text-slate-400 hover:text-primary transition-colors duration-200">首页</a></li>
            <li><a href="#features" class="text-slate-400 hover:text-primary transition-colors duration-200">特色玩法</a></li>
            <li><a href="#staff" class="text-slate-400 hover:text-primary transition-colors duration-200">管理团队</a></li>
            <li><a href="#join" class="text-slate-400 hover:text-primary transition-colors duration-200">加入我们</a></li>
          </ul>
        </div>

        <!-- Social / Contact -->
        <div>
          <h3 class="text-lg font-bold text-white mb-6">联系我们</h3>
          <ul class="space-y-4">
            <li class="flex items-center gap-2">
              <span class="text-slate-400">QQ 群:</span>
              <a href="#" class="text-primary hover:text-primary-light transition-colors duration-200">123456789</a>
            </li>
            <li class="flex items-center gap-2">
              <span class="text-slate-400">邮箱:</span>
              <a href="mailto:admin@wsmcs.net" class="text-primary hover:text-primary-light transition-colors duration-200">admin@wsmcs.net</a>
            </li>
          </ul>
        </div>
      </div>

      <!-- Copyright -->
      <div class="pt-8 border-t border-slate-800 flex flex-col md:flex-row justify-between items-center gap-4">
        <p class="text-slate-500 text-sm text-center md:text-left">
          &copy; {{ currentYear }} WSMCS. All rights reserved. Not an official Minecraft product. Not approved by or associated with Mojang.
        </p>
      </div>
    </div>
  </footer>
</template>
