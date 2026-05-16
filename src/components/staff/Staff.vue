<script setup lang="ts">
const staffMembers = [
  {
    id: 1,
    name: 'Admin_Steve',
    role: '服主 / 创始人',
    avatar: 'https://minotar.net/helm/Steve/200.png',
  },
  {
    id: 2,
    name: 'Dev_Alex',
    role: '核心开发者',
    avatar: 'https://minotar.net/helm/Alex/200.png',
  },
  {
    id: 3,
    name: 'Mod_Notch',
    role: '社区管理员',
    avatar: 'https://minotar.net/helm/Notch/200.png',
  },
  {
    id: 4,
    name: 'Builder_Jeb',
    role: '建筑师',
    avatar: 'https://minotar.net/helm/jeb_/200.png',
  }
];
</script>

<template>
  <section id="staff" class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Section Header -->
      <div class="text-center max-w-3xl mx-auto mb-16">
        <h2 class="text-3xl md:text-4xl font-extrabold text-slate-900 tracking-tight mb-4">
          管理团队
        </h2>
        <p class="text-lg text-slate-600">
          用心的管理与开发团队，为你提供最稳定、优质的游戏体验
        </p>
      </div>

      <!-- Staff Grid -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
        <div 
          v-for="staff in staffMembers" 
          :key="staff.id"
          class="bg-slate-50 rounded-3xl p-8 text-center shadow-[0_4px_20px_rgb(0,0,0,0.03)] hover:shadow-[0_8px_30px_rgb(0,0,0,0.08)] transition-all duration-300 transform hover:-translate-y-1 group border border-slate-100"
        >
          <!-- Avatar -->
          <div class="w-32 h-32 mx-auto mb-6 rounded-2xl overflow-hidden bg-slate-200 shadow-inner group-hover:scale-105 transition-transform duration-300">
            <img 
              :src="staff.avatar" 
              :alt="staff.name" 
              class="w-full h-full object-cover rendering-pixelated"
              style="image-rendering: pixelated;"
            />
          </div>
          
          <!-- Info -->
          <h3 class="text-xl font-bold text-slate-900 mb-2">
            {{ staff.name }}
          </h3>
          <p class="text-primary font-medium">
            {{ staff.role }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
