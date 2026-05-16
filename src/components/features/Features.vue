<script setup lang="ts">
const features = [
  {
    id: 1,
    title: '纯净生存',
    description: '原汁原味的生存体验，没有繁杂的插件和限制，和朋友一起从零开始建造属于你们的家园。',
    image: '/images/survival.webp',
  },
  {
    id: 2,
    title: '粘液科技',
    description: '丰富的科技树，自动化机器与独特的物品系统，突破原版的限制，体验工业化的乐趣。',
    image: '/images/slimefun.webp',
  },
  {
    id: 3,
    title: '起床战争',
    description: '激烈的 PVP 对战，保护你的床，摧毁敌人的床，运用策略和操作赢得最终的胜利。',
    image: '/images/bedwars.webp',
  }
];
</script>

<template>
  <section id="features" class="py-24 bg-slate-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Section Header -->
      <div class="text-center max-w-3xl mx-auto mb-16">
        <h2 class="text-3xl md:text-4xl font-extrabold text-slate-900 tracking-tight mb-4">
          特色玩法
        </h2>
        <p class="text-lg text-slate-600">
          多样化的游戏模式，满足你对 Minecraft 的所有想象
        </p>
      </div>

      <!-- Cards Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
        <div 
          v-for="feature in features" 
          :key="feature.id"
          class="bg-white rounded-3xl overflow-hidden shadow-[0_8px_30px_rgb(0,0,0,0.04)] hover:shadow-[0_8px_30px_rgb(0,0,0,0.12)] transition-all duration-300 transform hover:-translate-y-2 group"
        >
          <!-- Image Container -->
          <div class="aspect-[4/3] w-full overflow-hidden relative">
            <img 
              :src="feature.image" 
              :alt="feature.title" 
              class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"
            />
            <div class="absolute inset-0 bg-gradient-to-t from-slate-900/40 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          </div>
          
          <!-- Content Container -->
          <div class="p-8">
            <h3 class="text-2xl font-bold text-slate-900 mb-3 group-hover:text-primary transition-colors duration-300">
              {{ feature.title }}
            </h3>
            <p class="text-slate-600 leading-relaxed">
              {{ feature.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
