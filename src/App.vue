<!-- The exported code uses Tailwind CSS. Install Tailwind CSS in your dev environment to ensure all styles work. -->

<template>
  <div class="min-h-screen bg-gradient-to-b from-gray-900 to-indigo-900">
    <!-- 导航栏 -->
    <nav class="fixed w-full z-50 bg-opacity-80 bg-gray-900 backdrop-blur-md">
      <div class="max-w-7xl mx-auto px-4 h-20 flex items-center justify-between">
        <div class="text-3xl font-bold bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">
          CiumHoa
        </div>
        <div class="flex space-x-8">
          <a v-for="item in navItems" :key="item" class="text-gray-300 hover:text-white transition-colors cursor-pointer">
            {{ item }}
          </a>
        </div>
      </div>
    </nav>

    <!-- Hero区域 -->
    <div class="relative h-screen flex items-center justify-center overflow-hidden">
      <div class="absolute inset-0">
        <img :src="heroImage" class="w-full h-full object-cover" alt="hero background" />
      </div>
      <div class="relative z-10 text-center text-white max-w-4xl mx-auto px-4">
        <h1 class="text-5xl font-bold mb-6">引领未来科技，开创无限可能</h1>
        <p class="text-xl mb-8">致力于推动人类文明的进步，探索宇宙的奥秘，引领量子科技的革命</p>
        <div class="flex justify-center space-x-6">
          <button class="!rounded-button bg-blue-600 hover:bg-blue-700 text-white px-8 py-3">
            探索产品
          </button>
          <button class="!rounded-button border-2 border-white text-white px-8 py-3 hover:bg-white hover:text-gray-900">
            了解更多
          </button>
        </div>
      </div>
    </div>

    <!-- 产品展示区 -->
    <div class="max-w-7xl mx-auto px-4 py-20">
      <h2 class="text-4xl font-bold text-center text-white mb-16">前沿科技产品</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div v-for="product in products" :key="product.title" 
             class="bg-gray-800 rounded-xl overflow-hidden transform hover:scale-105 transition-transform">
          <img :src="product.image" class="w-full h-64 object-cover" :alt="product.title">
          <div class="p-6">
            <h3 class="text-xl font-bold text-white mb-2">{{ product.title }}</h3>
            <p class="text-gray-400 mb-4">{{ product.description }}</p>
            <button class="!rounded-button bg-blue-600 hover:bg-blue-700 text-white px-6 py-2">
              了解详情
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- 技术优势 -->
    <div class="bg-gray-800 py-20">
      <div class="max-w-7xl mx-auto px-4">
        <h2 class="text-4xl font-bold text-center text-white mb-16">核心优势</h2>
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
          <div v-for="advantage in advantages" :key="advantage.title" class="text-center">
            <el-icon class="text-5xl text-blue-500 mb-4" :size="48">
              <component :is="advantage.icon" />
            </el-icon>
            <h3 class="text-xl font-bold text-white mb-2">{{ advantage.title }}</h3>
            <p class="text-gray-400">{{ advantage.description }}</p>
          </div>
        </div>
      </div>
    </div>

    <!-- 新闻动态 -->
    <div class="max-w-7xl mx-auto px-4 py-20">
      <h2 class="text-4xl font-bold text-center text-white mb-16">最新动态</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div v-for="news in newsItems" :key="news.title" 
             class="bg-gray-800 rounded-xl overflow-hidden hover:shadow-xl transition-shadow">
          <img :src="news.image" class="w-full h-48 object-cover" :alt="news.title">
          <div class="p-6">
            <h3 class="text-xl font-bold text-white mb-2">{{ news.title }}</h3>
            <p class="text-gray-400 mb-4">{{ news.description }}</p>
            <div class="flex justify-between items-center">
              <span class="text-gray-500">{{ news.date }}</span>
              <button class="!rounded-button text-blue-500 hover:text-blue-400">
                阅读更多
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 合作伙伴 -->
    <div class="bg-gray-800 py-20">
      <div class="max-w-7xl mx-auto px-4">
        <h2 class="text-4xl font-bold text-center text-white mb-16">
          合作伙伴
        </h2>
        <swiper
          :modules="swiperModules"
          :slides-per-view="5"
          :space-between="30"
          :autoplay="{ delay: 3000 }"
          :loop="true"
          class="partner-swiper"
        >
          <swiper-slide v-for="partner in partners" :key="partner.name">
            <img
              :src="partner.logo"
              :alt="partner.name"
              class="h-16 object-contain mx-auto filter grayscale hover:grayscale-0 transition-all"
            />
          </swiper-slide>
        </swiper>
      </div>
    </div>

    <!-- 页脚 -->
    <footer class="bg-gray-900 pt-20 pb-10">
      <div class="max-w-7xl mx-auto px-4 grid grid-cols-1 md:grid-cols-4 gap-8">
        <div>
          <h3 class="text-xl font-bold text-white mb-4">关于我们</h3>
          <p class="text-gray-400">CiumHoa致力于推动科技创新，为人类创造更美好的未来。我们在太空探索、量子计算等领域持续突破，引领行业发展。</p>
        </div>
        <div>
          <h3 class="text-xl font-bold text-white mb-4">快速链接</h3>
          <ul class="space-y-2">
            <li v-for="link in footerLinks" :key="link">
              <a href="#" class="text-gray-400 hover:text-white">{{ link }}</a>
            </li>
          </ul>
        </div>
        <div>
          <h3 class="text-xl font-bold text-white mb-4">联系我们</h3>
          <ul class="space-y-2 text-gray-400">
            <li>电话：400-888-8888</li>
            <li>邮箱：contact@ciumhoa.com</li>
            <li>地址：长安市大唐新区科技创新中心</li>
          </ul>
        </div>
        <div>
          <h3 class="text-xl font-bold text-white mb-4">关注我们</h3>
          <div class="flex space-x-4">
            <el-icon v-for="icon in socialIcons" :key="icon" class="text-gray-400 hover:text-white cursor-pointer" :size="24">
              <component :is="icon" />
            </el-icon>
          </div>
        </div>
      </div>
      <div class="mt-16 text-center text-gray-500">
        <p>© 2025 CiumHoa Technology. All rights reserved. 华ICP备20250520号-1</p>
      </div>
    </footer>
  </div>
</template>

<script lang="ts" setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Pagination, Autoplay } from 'swiper/modules';
// @ts-ignore
import "swiper/css";
// @ts-ignore
import "swiper/css/navigation";
// @ts-ignore
import "swiper/css/pagination";
// @ts-ignore
import {
  Monitor,
  Share,
  Connection,
  Cpu,
  Message,
  Link,
  Star
} from '@element-plus/icons-vue';

const swiperModules = [Pagination, Autoplay];

const heroImage = '/7bf59dc0c13557af9d20be12478603b9.jpg';

const navItems = ['首页', '产品中心', '技术创新', '关于我们', '联系方式'];

const products = [
  {
    title: '量子计算机',
    description: '突破性的量子计算技术，为复杂计算提供革命性解决方案',
    image: '/4599eb3beab7ede1c52c85ced2aad1b3.jpg'
  },
  {
    title: '太空探测器',
    description: '新一代深空探测设备，助力人类探索宇宙奥秘',
    image: '/c41a8f87868e83a91c65685e2fafecca.jpg'
  },
  {
    title: '清洁能源系统',
    description: '革命性清洁能源解决方案，引领绿色科技发展',
    image: '/ae810d23a914bb2f77bef7aed8d581a5.jpg'
  }
];

const advantages = [
  {
    icon: 'Monitor',
    title: '尖端研发能力',
    description: '拥有全球顶尖的研发团队和实验室'
  },
  {
    icon: 'Share',
    title: '全球专利技术',
    description: '数千项核心技术专利，引领行业发展'
  },
  {
    icon: 'Connection',
    title: '国际合作网络',
    description: '与全球顶尖研究机构展开深度合作'
  },
  {
    icon: 'Cpu',
    title: '创新解决方案',
    description: '为客户提供定制化的技术解决方案'
  }
];

const newsItems = [
  {
    title: '突破性量子纠缠实验成功',
    description: '我司成功实现了千公里级量子纠缠态的稳定传输',
    date: '2025-03-01',
    image: '/4d7cd78538da63652913cbd6de4956d7.jpg'
  },
  {
    title: '新一代太阳能技术发布',
    description: '转化效率突破50%，开创清洁能源新纪元',
    date: '2025-02-28',
    image: '/ca5891954f08d66192380193568fff6d.jpg'
  },
  {
    title: '深空探测器成功发射',
    description: '开启人类探索太阳系外行星的新篇章',
    date: '2025-02-25',
    image: '/45f731ab05492124d889ac7649c3f0d9.jpg'
  }
];

const partners = [
  {
    name: '全球科技',
    logo: '/2cab55193b0409f9b49cb420f64a71d5.jpg'
  },
  {
    name: '未来研究院',
    logo: '/a724d92d1cd30a5272f6bfc0b4f2eaa8.jpg'
  },
  {
    name: '量子科技',
    logo: '/9046c29fa373659c16a261f683cb07a2.jpg'
  },
  {
    name: '星际探索',
    logo: '/74d246ff916a4d12c25d43bf2937d901.jpg'
  },
  {
    name: '能源创新',
    logo: '/80fbaa8b1ba92a6f3e7862c705c23de6.jpg'
  }
];

const footerLinks = ['公司简介', '产品服务', '新闻中心', '加入我们', '投资者关系'];
const socialIcons = [Message, Link, Star];
</script>

<style scoped>
.partner-swiper {
  padding: 20px 0;
}

.custom-gradient {
  background: linear-gradient(135deg, #1a365d 0%, #2d3748 100%);
}
</style>

