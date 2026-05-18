<script setup lang="ts">
import Button from '../components/ui/Button.vue'
import SectionTitle from '../components/ui/SectionTitle.vue'
import FeatureCard from '../components/common/FeatureCard.vue'
import TeamCard from '../components/common/TeamCard.vue'

// Images
import heroBg from '../assets/images/hero-bg.png'
import feature1Bg from '../assets/images/feature-1.png'
import feature2Bg from '../assets/images/feature-2.png'
import feature3Bg from '../assets/images/feature-3.png'

import avatar1 from '../assets/images/avatar-1.png'
import avatar2 from '../assets/images/avatar-2.png'
import avatar3 from '../assets/images/avatar-3.png'
import avatar4 from '../assets/images/avatar-4.png'
import avatar5 from '../assets/images/avatar-5.png'
import avatar6 from '../assets/images/avatar-6.png'
import avatar7 from '../assets/images/avatar-7.png'

const teamAvatars = [
  avatar1,
  avatar2,
  avatar3,
  avatar4,
  avatar5,
  avatar6,
  avatar7
]

const teamMembers = [
  {
    name: 'ApartTUSITU',
    description: '服务器技术 & 各项服务运营',
    avatarSrc: teamAvatars[0],
    tags: [{ label: '服主' }]
  },
  {
    name: 'Tom_Chicken',
    description: '与 FrankHymC 创立 WSMCS',
    avatarSrc: teamAvatars[1],
    tags: [{ label: '资金支持' }, { label: '创始人' }] // Stacked in design
  },
  {
    name: 'FrankHymC',
    description: '与 Tom_Chicken 创立 WSMCS',
    avatarSrc: teamAvatars[2],
    tags: [{ label: '资金支持' }, { label: '创始人' }]
  },
  {
    name: 'H_WZS_CoCo',
    description: '服务器运营',
    avatarSrc: teamAvatars[3],
    tags: [{ label: '管理' }]
  },
  {
    name: 'Steve_Officials',
    description: '服务器支持',
    avatarSrc: teamAvatars[4],
    tags: [{ label: '管理' }]
  },
  {
    name: 'Sean20211012',
    description: '服务器运营',
    avatarSrc: teamAvatars[5],
    tags: [{ label: '管理' }]
  },
  {
    name: 'Alves',
    description: '服务器运营',
    avatarSrc: teamAvatars[6],
    tags: [{ label: '管理' }]
  }
]
</script>

<template>
  <div class="w-full relative">
    
    <!-- Hero Section -->
    <section class="relative h-[770px] w-full bg-black">
      <img :src="heroBg" alt="Hero Background" class="absolute inset-0 w-full h-full object-cover pointer-events-none" />
      
      <div class="absolute inset-0 bg-black/10"></div> <!-- Slight overlay if needed -->
      
      <div class="relative z-10 max-w-[1440px] mx-auto h-full w-full">
        <!-- Content aligned to Figma specs: left-[90px] top-[243px] inside 1440px container -->
        <div class="absolute left-6 md:left-[90px] top-[243px]">
          <h1 class="text-white font-semibold text-[48px] md:text-[64px] leading-tight mb-[30px]">
            繁星之望服务器
          </h1>
          <div class="text-white/65 font-medium text-[20px] md:text-[24px] leading-snug max-w-[546px] mb-[40px]">
            <p>一个拥有诸多优点的 Minecraft 高性能养老服务器</p>
            <p>时刻欢迎广大玩家加入。</p>
          </div>
          <div class="flex flex-wrap items-center gap-[17px]">
            <Button variant="primary">加入QQ群</Button>
            <Button variant="secondary">加入游戏</Button>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="w-full bg-white pt-[64px] pb-[100px]">
      <div class="max-w-[1206px] mx-auto px-6 lg:px-0">
        <SectionTitle 
          title="精心打造的玩法"
          description="我们有着原版生存、粘液单方块空岛、起床战争三个子服。 我们会不断持续添加新的游戏玩法，以及激动人心的活动，为玩家提供新鲜刺激的游戏体验。 无论探险，还是 PvP，我们都有适合你的游戏内容。"
        />
        
        <!-- Grid layout matching Figma width constraints: 529px, 311px, 311px, gap 29px -->
        <div class="flex flex-col lg:flex-row gap-[29px] mt-[40px] h-auto lg:h-[486px]">
          <div class="w-full lg:w-[529px] h-[486px]">
            <FeatureCard 
              title="原版生存"
              description="体验最纯净的高版本原版生存，可以化作生电大佬，也可以在一方静谧之中享受游戏人生。 我们尽量保证玩家的高自由度，让玩家在原汁原味的 Minecraft 体验中感到快乐。"
              :imageSrc="feature1Bg"
            />
          </div>
          <div class="w-full lg:w-[311px] h-[486px]">
            <FeatureCard 
              title="粘液单方块空岛"
              description="将 Minecraft、单方块空岛、粘液科技结合，打造专属于玩家的科技环境。 玩家一人一岛，通过一个小方块，构建一个大世界。"
              :imageSrc="feature2Bg"
            />
          </div>
          <div class="w-full lg:w-[311px] h-[486px]">
            <FeatureCard 
              title="起床战争"
              description="1:1 复刻 Hypixel Bedwards，感受 PvP 的趣味。 团队协作，亦或是独自奋战，赢得比赛胜利。"
              :imageSrc="feature3Bg"
            />
          </div>
        </div>
      </div>
    </section>

    <!-- Team Section -->
    <section class="w-full bg-white pt-[15px] pb-[100px]">
      <div class="max-w-[1206px] mx-auto px-6 lg:px-0">
        <SectionTitle 
          title="专业的管理团队"
          description="我们的工作室成员活跃，充分做到与玩家热情互动， 管理组办事雷厉风行，保证玩家的游玩体验。"
        />
        
        <!-- 3 columns grid, gap 21px -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-[21px] mt-[40px]">
          <TeamCard 
            v-for="(member, index) in teamMembers" 
            :key="index"
            :name="member.name"
            :description="member.description"
            :avatarSrc="member.avatarSrc"
            :tags="member.tags"
          />
        </div>
      </div>
    </section>

    <!-- Join Banner Section -->
    <section class="w-full h-[256px] relative overflow-hidden flex items-center justify-center">
      <img :src="heroBg" alt="Join Background" class="absolute inset-0 w-full h-full object-cover pointer-events-none" />
      <div class="absolute inset-0 bg-black/36"></div>
      
      <div class="relative z-10 flex flex-col items-center justify-center w-full max-w-[1440px] text-center">
        <h2 class="text-white font-semibold text-[36px] mb-[12px]">
          立即加入 繁星之望
        </h2>
        <p class="text-white/80 font-medium text-[16px] mb-[12px]">
          1.13-1.21.3 Java 版 / 最新基岩版
        </p>
        <!-- The IP Box -->
        <div class="bg-white/80 backdrop-blur-sm rounded-[10px] w-[348px] h-[47px] flex items-center justify-center shadow-sm">
          <span class="text-black font-medium text-[20px]">
            server.wsmcs.top
          </span>
        </div>
        <p class="text-white/80 text-[12px] mt-2">
          通过正版、LittleSkin、红石皮肤站进入服务器。
        </p>
      </div>
    </section>

  </div>
</template>
