<!-- The exported code uses Tailwind CSS. Install Tailwind CSS in your dev environment to ensure all styles work. -->

<template>
    <div class="min-h-screen bg-gradient-to-b from-slate-900 via-indigo-950 to-slate-900 text-white">
      <!-- 导航栏 -->
      <header class="fixed top-0 left-0 right-0 z-50 bg-opacity-80 bg-slate-900 backdrop-blur-md transition-all duration-300">
        <div class="container mx-auto px-6 py-4 flex items-center justify-between">
          <div class="flex items-center">
            <h1 class="text-2xl font-bold bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">
              CiumHoa <span class="text-lg">中华科技</span>
            </h1>
          </div>
          
          <nav class="hidden md:flex items-center space-x-8">
            <a href="#" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer whitespace-nowrap">首页</a>
            <a href="#future-tech" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer whitespace-nowrap">未来科技</a>
            <a href="#solutions" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer whitespace-nowrap">行业解决方案</a>
            <a href="#about" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer whitespace-nowrap">关于CiumHoa</a>
            <a href="#research" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer whitespace-nowrap">研究院与实验室</a>
            <a href="#media" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer whitespace-nowrap">媒体中心</a>
            <a href="#contact" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer whitespace-nowrap">联系我们</a>
          </nav>
          
          <div class="flex items-center space-x-4">
            <button class="bg-blue-600 hover:bg-blue-700 text-white px-4 py-2 rounded-lg transition-colors duration-300 cursor-pointer !rounded-button whitespace-nowrap">
              中 / EN
            </button>
            <button class="md:hidden text-white cursor-pointer" @click="toggleMobileMenu">
              <el-icon><Menu /></el-icon>
            </button>
          </div>
        </div>
        
        <!-- 移动端菜单 -->
        <div v-if="mobileMenuOpen" class="md:hidden bg-slate-800 bg-opacity-95 backdrop-blur-md">
          <div class="container mx-auto px-6 py-4 flex flex-col space-y-4">
            <a href="#" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer">首页</a>
            <a href="#future-tech" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer">未来科技</a>
            <a href="#solutions" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer">行业解决方案</a>
            <a href="#about" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer">关于CiumHoa</a>
            <a href="#research" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer">研究院与实验室</a>
            <a href="#media" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer">媒体中心</a>
            <a href="#contact" class="text-white hover:text-blue-400 transition-colors duration-300 cursor-pointer">联系我们</a>
          </div>
        </div>
      </header>
  
      <!-- Hero 区域 -->
      <section class="relative h-screen flex items-center overflow-hidden" style="background-image: url('/img_2.jpg')">
        <div class="absolute inset-0 bg-gradient-to-r from-slate-900/90 to-transparent"></div>
        <div class="container mx-auto px-6 relative z-10 flex flex-col md:flex-row items-center">
          <div class="md:w-1/2 mb-10 md:mb-0">
            <h1 class="text-4xl md:text-6xl font-bold mb-4 leading-tight">
              <span class="bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">科技溯源东方，智慧绽放全球</span>
            </h1>
            <p class="text-xl md:text-2xl mb-8 text-blue-100">CiumHoa 中华科技 — 赋能人类文明的未来引擎</p>
            <div class="flex flex-wrap gap-4">
              <button class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-lg transition-colors duration-300 text-lg cursor-pointer !rounded-button whitespace-nowrap">
                探索未来科技
              </button>
              <button class="bg-transparent border border-blue-400 hover:bg-blue-900/30 text-blue-300 px-6 py-3 rounded-lg transition-colors duration-300 text-lg cursor-pointer !rounded-button whitespace-nowrap">
                了解我们的使命
              </button>
            </div>
          </div>
        </div>
        
        <!-- 动态粒子效果 -->
        <div ref="particlesContainer" class="absolute inset-0 z-0"></div>
      </section>
  
      <!-- 公司愿景与使命 -->
      <section class="py-20 bg-slate-900/80">
        <div class="container mx-auto px-6">
          <h2 class="text-3xl md:text-4xl font-bold text-center mb-16 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">公司愿景与使命</h2>
          
          <div class="flex flex-col md:flex-row items-center gap-10">
            <div class="md:w-1/2">
              <img src="/img_25.jpg" alt="中华科技愿景" class="rounded-xl shadow-2xl shadow-blue-900/50 w-full h-auto object-cover">
            </div>
            
            <div class="md:w-1/2 space-y-8">
              <div class="bg-slate-800/50 backdrop-blur-sm p-6 rounded-xl border-l-4 border-blue-500">
                <h3 class="text-xl font-bold mb-3 text-blue-300">植根中华智慧</h3>
                <p class="text-gray-300">我们深入挖掘五千年中华文明精髓，将传统智慧与现代科技完美融合，创造具有东方特色的创新解决方案。</p>
              </div>
              
              <div class="bg-slate-800/50 backdrop-blur-sm p-6 rounded-xl border-l-4 border-purple-500">
                <h3 class="text-xl font-bold mb-3 text-purple-300">引领未来科技</h3>
                <p class="text-gray-300">通过前瞻性研究与开发，我们致力于在量子通信、脑机接口、人工智能等领域突破创新，塑造人类科技未来。</p>
              </div>
              
              <div class="bg-slate-800/50 backdrop-blur-sm p-6 rounded-xl border-l-4 border-indigo-500">
                <h3 class="text-xl font-bold mb-3 text-indigo-300">建构全球连接</h3>
                <p class="text-gray-300">我们构建开放合作的全球创新网络，连接世界顶尖人才与资源，共同应对人类面临的重大挑战。</p>
              </div>
            </div>
          </div>
        </div>
      </section>
  
      <!-- 未来科技矩阵 -->
      <section id="future-tech" class="py-20 bg-gradient-to-b from-slate-900 to-indigo-950">
        <div class="container mx-auto px-6">
          <h2 class="text-3xl md:text-4xl font-bold text-center mb-4 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">未来科技矩阵</h2>
          <p class="text-center text-blue-200 mb-16 max-w-3xl mx-auto">探索 CiumHoa 中华科技前沿研发的尖端技术，这些创新将重塑人类未来生活与工作方式</p>
          
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <div v-for="(tech, index) in futureTechnologies" :key="index" 
                 class="bg-slate-800/30 backdrop-blur-md rounded-xl overflow-hidden transition-all duration-500 hover:shadow-xl hover:shadow-blue-900/30 hover:-translate-y-2 group cursor-pointer">
              <div class="h-48 overflow-hidden">
                <img :src="tech.image" :alt="tech.title" class="w-full h-full object-cover object-top transition-transform duration-700 group-hover:scale-110">
              </div>
              <div class="p-6">
                <h3 class="text-xl font-bold mb-3 text-blue-300">{{ tech.title }}</h3>
                <p class="text-gray-300 mb-4">{{ tech.description }}</p>
                <div class="flex flex-wrap gap-2">
                  <span v-for="(tag, tagIndex) in tech.tags" :key="tagIndex" 
                        class="text-xs px-3 py-1 rounded-full bg-blue-900/50 text-blue-200">
                    {{ tag }}
                  </span>
                </div>
                <button class="mt-6 text-blue-400 hover:text-blue-300 flex items-center gap-2 transition-colors cursor-pointer !rounded-button whitespace-nowrap">
                  了解更多 <el-icon><ArrowRight /></el-icon>
                </button>
              </div>
            </div>
          </div>
        </div>
      </section>
  
      <!-- 行业解决方案 -->
      <section id="solutions" class="py-20 bg-slate-900 relative overflow-hidden">
        <div class="absolute top-0 left-0 w-full h-full opacity-10" 
             style="background-image: url('/img_28.jpg'); background-size: cover;"></div>
        
        <div class="container mx-auto px-6 relative z-10">
          <h2 class="text-3xl md:text-4xl font-bold text-center mb-4 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">行业解决方案</h2>
          <p class="text-center text-blue-200 mb-16 max-w-3xl mx-auto">我们的前沿科技与行业深度融合，为各领域提供定制化的未来解决方案</p>
          
          <div class="flex flex-col lg:flex-row gap-8">
            <!-- 左侧导航 -->
            <div class="lg:w-1/4">
              <div class="bg-slate-800/50 backdrop-blur-sm rounded-xl p-4 sticky top-24">
                <h3 class="text-xl font-bold mb-6 text-center text-blue-300">解决方案领域</h3>
                <div class="space-y-2">
                  <button v-for="(solution, index) in industrySolutions" :key="index"
                          @click="selectedSolution = index"
                          :class="[
                            'w-full text-left px-4 py-3 rounded-lg transition-all duration-300 cursor-pointer !rounded-button whitespace-nowrap',
                            selectedSolution === index 
                              ? 'bg-blue-600 text-white' 
                              : 'bg-slate-700/50 text-gray-300 hover:bg-slate-700'
                          ]">
                    {{ solution.title }}
                  </button>
                </div>
              </div>
            </div>
            
            <!-- 右侧内容 -->
            <div class="lg:w-3/4">
              <div class="bg-slate-800/30 backdrop-blur-md rounded-xl overflow-hidden">
                <div class="h-64 md:h-80 overflow-hidden">
                  <img :src="industrySolutions[selectedSolution].image" :alt="industrySolutions[selectedSolution].title" class="w-full h-full object-cover object-top">
                </div>
                <div class="p-8">
                  <h3 class="text-2xl font-bold mb-4 text-blue-300">{{ industrySolutions[selectedSolution].title }}</h3>
                  <p class="text-gray-300 mb-6">{{ industrySolutions[selectedSolution].description }}</p>
                  
                  <h4 class="text-lg font-semibold mb-3 text-purple-300">核心技术</h4>
                  <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                    <div v-for="(tech, techIndex) in industrySolutions[selectedSolution].technologies" :key="techIndex"
                         class="bg-slate-700/50 p-4 rounded-lg flex items-start gap-3">
                      <el-icon class="text-blue-400 text-xl mt-1"><Monitor /></el-icon>
                      <div>
                        <h5 class="font-semibold text-blue-200">{{ tech.name }}</h5>
                        <p class="text-sm text-gray-400">{{ tech.description }}</p>
                      </div>
                    </div>
                  </div>
                  
                  <div class="flex justify-end">
                    <button class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-lg transition-colors duration-300 flex items-center gap-2 cursor-pointer !rounded-button whitespace-nowrap">
                      获取解决方案 <el-icon><ArrowRight /></el-icon>
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
  
      <!-- 研究院与实验室 -->
      <section id="research" class="py-20 bg-gradient-to-b from-indigo-950 to-slate-900">
        <div class="container mx-auto px-6">
          <h2 class="text-3xl md:text-4xl font-bold text-center mb-4 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">CiumHoa Future Lab™</h2>
          <p class="text-center text-blue-200 mb-16 max-w-3xl mx-auto">我们的未来研究院汇聚全球顶尖科学家，探索突破性技术与理念</p>
          
          <div class="relative">
            <!-- 中心图标 -->
            <div class="absolute left-1/2 top-1/2 transform -translate-x-1/2 -translate-y-1/2 hidden lg:block">
              <div class="w-40 h-40 rounded-full bg-blue-900/30 backdrop-blur-md flex items-center justify-center border border-blue-500/50 shadow-lg shadow-blue-500/20">
                <h3 class="text-xl font-bold text-center text-blue-300">CiumHoa<br>Future Lab™</h3>
              </div>
            </div>
            
            <!-- 实验室展示 -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
              <div v-for="(lab, index) in researchLabs" :key="index"
                   class="bg-slate-800/30 backdrop-blur-md rounded-xl overflow-hidden transition-all duration-500 hover:shadow-xl hover:shadow-blue-900/30 hover:-translate-y-2 cursor-pointer">
                <div class="h-48 overflow-hidden">
                  <img :src="lab.image" :alt="lab.name" class="w-full h-full object-cover object-top">
                </div>
                <div class="p-6">
                  <h3 class="text-xl font-bold mb-3 text-blue-300">{{ lab.name }}</h3>
                  <p class="text-gray-300 mb-4">{{ lab.description }}</p>
                  <div class="flex flex-wrap gap-2">
                    <span v-for="(area, areaIndex) in lab.researchAreas" :key="areaIndex" 
                          class="text-xs px-3 py-1 rounded-full bg-blue-900/50 text-blue-200">
                      {{ area }}
                    </span>
                  </div>
                </div>
              </div>
            </div>
          </div>
          
          <!-- 合作机构 -->
          <div class="mt-20">
            <h3 class="text-2xl font-bold text-center mb-10 text-blue-300">全球合作伙伴</h3>
            <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-8">
              <div v-for="(partner, index) in partners" :key="index" 
                   class="flex flex-col items-center justify-center p-4 bg-slate-800/30 backdrop-blur-md rounded-xl hover:bg-slate-800/50 transition-colors cursor-pointer">
                <el-icon class="text-4xl mb-3 text-gray-400"><component :is="partner.icon" /></el-icon>
                <span class="text-center text-sm text-gray-300">{{ partner.name }}</span>
              </div>
            </div>
          </div>
        </div>
      </section>
  
      <!-- 未来指数 -->
      <section class="py-20 bg-slate-900">
        <div class="container mx-auto px-6">
          <h2 class="text-3xl md:text-4xl font-bold text-center mb-4 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">未来科技指数</h2>
          <p class="text-center text-blue-200 mb-16 max-w-3xl mx-auto">实时追踪 CiumHoa 中华科技在各前沿领域的研发进展与投入</p>
          
          <div class="bg-slate-800/30 backdrop-blur-md rounded-xl p-6 md:p-10">
            <div ref="techIndexChart" class="w-full h-80"></div>
          </div>
        </div>
      </section>
  
      <!-- 媒体中心 -->
      <section id="media" class="py-20 bg-gradient-to-b from-slate-900 to-indigo-950">
        <div class="container mx-auto px-6">
          <h2 class="text-3xl md:text-4xl font-bold text-center mb-4 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">媒体中心</h2>
          <p class="text-center text-blue-200 mb-16 max-w-3xl mx-auto">了解 CiumHoa 中华科技的最新动态、研究成果与行业洞察</p>
          
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <div v-for="(article, index) in newsArticles" :key="index"
                 class="bg-slate-800/30 backdrop-blur-md rounded-xl overflow-hidden transition-all duration-500 hover:shadow-xl hover:shadow-blue-900/30 hover:-translate-y-2 cursor-pointer">
              <div class="h-48 overflow-hidden">
                <img :src="article.image" :alt="article.title" class="w-full h-full object-cover object-top">
              </div>
              <div class="p-6">
                <div class="flex justify-between items-center mb-3">
                  <span class="text-xs px-3 py-1 rounded-full bg-blue-900/50 text-blue-200">{{ article.category }}</span>
                  <span class="text-sm text-gray-400">{{ article.date }}</span>
                </div>
                <h3 class="text-xl font-bold mb-3 text-blue-300">{{ article.title }}</h3>
                <p class="text-gray-300 mb-4 line-clamp-3">{{ article.summary }}</p>
                <button class="text-blue-400 hover:text-blue-300 flex items-center gap-2 transition-colors cursor-pointer !rounded-button whitespace-nowrap">
                  阅读全文 <el-icon><ArrowRight /></el-icon>
                </button>
              </div>
            </div>
          </div>
          
          <div class="flex justify-center mt-10">
            <button class="bg-transparent border border-blue-400 hover:bg-blue-900/30 text-blue-300 px-6 py-3 rounded-lg transition-colors duration-300 cursor-pointer !rounded-button whitespace-nowrap">
              查看更多文章
            </button>
          </div>
        </div>
      </section>
  
      <!-- 联系我们 -->
      <section id="contact" class="py-20 bg-slate-900 relative">
        <div class="absolute top-0 left-0 w-full h-full opacity-10" 
             style="background-image: url('/img_18.jpg'); background-size: cover;"></div>
        
        <div class="container mx-auto px-6 relative z-10">
          <h2 class="text-3xl md:text-4xl font-bold text-center mb-4 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">联系我们</h2>
          <p class="text-center text-blue-200 mb-16 max-w-3xl mx-auto">无论您是寻求合作、了解产品，还是加入我们的团队，我们期待与您沟通</p>
          
          <div class="flex flex-col lg:flex-row gap-10">
            <div class="lg:w-1/2">
              <div class="bg-slate-800/30 backdrop-blur-md rounded-xl p-8">
                <h3 class="text-2xl font-bold mb-6 text-blue-300">发送消息</h3>
                
                <div class="space-y-4">
                  <div>
                    <label class="block text-sm font-medium text-gray-300 mb-1">您的姓名</label>
                    <input type="text" class="w-full px-4 py-2 bg-slate-700/50 border border-slate-600 rounded-lg focus:outline-none focus:border-blue-500 text-white" placeholder="请输入您的姓名">
                  </div>
                  
                  <div>
                    <label class="block text-sm font-medium text-gray-300 mb-1">电子邮箱</label>
                    <input type="email" class="w-full px-4 py-2 bg-slate-700/50 border border-slate-600 rounded-lg focus:outline-none focus:border-blue-500 text-white" placeholder="请输入您的电子邮箱">
                  </div>
                  
                  <div>
                    <label class="block text-sm font-medium text-gray-300 mb-1">咨询主题</label>
                    <select class="w-full px-4 py-2 bg-slate-700/50 border border-slate-600 rounded-lg focus:outline-none focus:border-blue-500 text-white appearance-none">
                      <option>产品咨询</option>
                      <option>技术合作</option>
                      <option>投资关系</option>
                      <option>加入我们</option>
                      <option>其他问题</option>
                    </select>
                  </div>
                  
                  <div>
                    <label class="block text-sm font-medium text-gray-300 mb-1">您的留言</label>
                    <textarea rows="4" class="w-full px-4 py-2 bg-slate-700/50 border border-slate-600 rounded-lg focus:outline-none focus:border-blue-500 text-white" placeholder="请详细描述您的需求或问题"></textarea>
                  </div>
                  
                  <button class="w-full bg-blue-600 hover:bg-blue-700 text-white px-6 py-3 rounded-lg transition-colors duration-300 cursor-pointer !rounded-button whitespace-nowrap">
                    发送留言
                  </button>
                </div>
              </div>
            </div>
            
            <div class="lg:w-1/2">
              <div class="bg-slate-800/30 backdrop-blur-md rounded-xl p-8 h-full">
                <h3 class="text-2xl font-bold mb-6 text-blue-300">联系方式</h3>
                
                <div class="space-y-6">
                  <div class="flex items-start gap-4">
                    <div class="bg-blue-900/50 p-3 rounded-lg">
                      <el-icon class="text-blue-300 text-xl"><Location /></el-icon>
                    </div>
                    <div>
                      <h4 class="font-semibold text-blue-200 mb-1">总部地址</h4>
                      <p class="text-gray-300">长安市大唐新区中华科技大厦</p>
                    </div>
                  </div>
                  
                  <div class="flex items-start gap-4">
                    <div class="bg-blue-900/50 p-3 rounded-lg">
                      <el-icon class="text-blue-300 text-xl"><Phone /></el-icon>
                    </div>
                    <div>
                      <h4 class="font-semibold text-blue-200 mb-1">联系电话</h4>
                      <p class="text-gray-300">+86 10 8888 8888</p>
                    </div>
                  </div>
                  
                  <div class="flex items-start gap-4">
                    <div class="bg-blue-900/50 p-3 rounded-lg">
                      <el-icon class="text-blue-300 text-xl"><Message /></el-icon>
                    </div>
                    <div>
                      <h4 class="font-semibold text-blue-200 mb-1">电子邮箱</h4>
                      <p class="text-gray-300">contact@ciumhoa.com</p>
                    </div>
                  </div>
                  
                  <div class="pt-6 border-t border-slate-700">
                    <h4 class="font-semibold text-blue-200 mb-4">全球分支机构</h4>
                    <div class="grid grid-cols-2 gap-4">
                      <div class="bg-slate-700/50 p-3 rounded-lg">
                        <h5 class="font-medium text-blue-200 mb-1">上海</h5>
                        <p class="text-sm text-gray-400">浦东新区张江高科技园区</p>
                      </div>
                      <div class="bg-slate-700/50 p-3 rounded-lg">
                        <h5 class="font-medium text-blue-200 mb-1">深圳</h5>
                        <p class="text-sm text-gray-400">南山区科技园</p>
                      </div>
                      <div class="bg-slate-700/50 p-3 rounded-lg">
                        <h5 class="font-medium text-blue-200 mb-1">硅谷</h5>
                        <p class="text-sm text-gray-400">加利福尼亚州帕洛阿尔托</p>
                      </div>
                      <div class="bg-slate-700/50 p-3 rounded-lg">
                        <h5 class="font-medium text-blue-200 mb-1">新加坡</h5>
                        <p class="text-sm text-gray-400">滨海湾金融中心</p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
  
      <!-- 页脚 -->
      <footer class="bg-slate-950 py-16">
        <div class="container mx-auto px-6">
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-10">
            <div>
              <h3 class="text-xl font-bold mb-6 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">CiumHoa 中华科技</h3>
              <p class="text-gray-400 mb-6">植根中华，开拓未来<br>科技之花，为世界绽放</p>
              <div class="flex space-x-4">
                <a href="#" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">
                  <el-icon><Message /></el-icon>
                </a>
                <a href="#" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">
                  <el-icon><Link /></el-icon>
                </a>
                <a href="#" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">
                  <el-icon><ChatDotRound /></el-icon>
                </a>
                <a href="#" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">
                  <el-icon><VideoPlay /></el-icon>
                </a>
              </div>
            </div>
            
            <div>
              <h4 class="text-lg font-semibold mb-4 text-gray-200">快速链接</h4>
              <ul class="space-y-2">
                <li><a href="#" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">首页</a></li>
                <li><a href="#future-tech" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">未来科技</a></li>
                <li><a href="#solutions" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">行业解决方案</a></li>
                <li><a href="#about" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">关于我们</a></li>
                <li><a href="#research" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">研究院与实验室</a></li>
                <li><a href="#media" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">媒体中心</a></li>
                <li><a href="#contact" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">联系我们</a></li>
              </ul>
            </div>
            
            <div>
              <h4 class="text-lg font-semibold mb-4 text-gray-200">法律信息</h4>
              <ul class="space-y-2">
                <li><a href="#" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">隐私政策</a></li>
                <li><a href="#" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">使用条款</a></li>
                <li><a href="#" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">知识产权</a></li>
                <li><a href="#" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">Cookie 政策</a></li>
                <li><a href="#" class="text-gray-400 hover:text-blue-400 transition-colors cursor-pointer">网站地图</a></li>
              </ul>
            </div>
            
            <div>
              <h4 class="text-lg font-semibold mb-4 text-gray-200">订阅未来科技简报</h4>
              <p class="text-gray-400 mb-4">定期获取前沿科技资讯与研究进展</p>
              <div class="flex">
                <input type="email" class="flex-1 px-4 py-2 bg-slate-800 border border-slate-700 rounded-l-lg focus:outline-none focus:border-blue-500 text-white" placeholder="您的电子邮箱">
                <button class="bg-blue-600 hover:bg-blue-700 text-white px-4 py-2 rounded-r-lg transition-colors duration-300 cursor-pointer !rounded-button whitespace-nowrap">
                  订阅
                </button>
              </div>
            </div>
          </div>
          
          <div class="mt-12 pt-8 border-t border-slate-800 flex flex-col md:flex-row justify-between items-center">
            <p class="text-gray-500 mb-4 md:mb-0">© 2025 CiumHoa 中华科技（集团）有限公司. 保留所有权利.</p>
            <div class="flex space-x-6">
              <el-icon class="text-gray-500"><CreditCard /></el-icon>
              <el-icon class="text-gray-500"><Money /></el-icon>
              <el-icon class="text-gray-500"><Wallet /></el-icon>
            </div>
          </div>
        </div>
      </footer>
  
      <!-- AI 助手悬浮窗 -->
      <div class="fixed bottom-8 right-8 z-50">
        <button @click="toggleAIAssistant" class="bg-blue-600 hover:bg-blue-700 w-16 h-16 rounded-full flex items-center justify-center shadow-lg shadow-blue-900/50 transition-all duration-300 cursor-pointer !rounded-button whitespace-nowrap">
          <el-icon v-if="!showAIAssistant" class="text-2xl text-white"><ChatDotRound /></el-icon>
          <el-icon v-else class="text-2xl text-white"><Close /></el-icon>
        </button>
        
        <div v-if="showAIAssistant" class="absolute bottom-20 right-0 w-80 bg-slate-800 rounded-xl shadow-xl shadow-blue-900/30 overflow-hidden transition-all duration-500">
          <div class="bg-gradient-to-r from-blue-600 to-purple-600 p-4">
            <div class="flex items-center gap-3">
              <div class="w-10 h-10 rounded-full bg-white/20 flex items-center justify-center">
                <el-icon class="text-white text-xl"><ChatDotRound /></el-icon>
              </div>
              <div>
                <h4 class="font-bold text-white">花智</h4>
                <p class="text-xs text-blue-100">CiumHoa AI 助手</p>
              </div>
            </div>
          </div>
          
          <div class="h-80 p-4 overflow-y-auto bg-slate-900">
            <div class="flex flex-col gap-3">
              <div class="bg-slate-800 p-3 rounded-lg max-w-[80%]">
                <p class="text-sm text-white">您好！我是花智，CiumHoa 中华科技的 AI 助手。有什么我可以帮助您的吗？</p>
              </div>
            </div>
          </div>
          
          <div class="p-3 bg-slate-800 border-t border-slate-700">
            <div class="flex gap-2">
              <input type="text" class="flex-1 px-4 py-2 bg-slate-700 border-none rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 text-white text-sm" placeholder="输入您的问题...">
              <button class="bg-blue-600 hover:bg-blue-700 px-3 py-2 rounded-lg transition-colors duration-300 cursor-pointer !rounded-button whitespace-nowrap">
                <el-icon class="text-white"><Position /></el-icon>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script lang="ts" setup>
  import { ref, onMounted, nextTick } from 'vue';
  import * as echarts from 'echarts';
  import { 
    Menu, ArrowRight, Monitor, Location, Phone, Message, Link, 
    ChatDotRound, VideoPlay, CreditCard, Money, Wallet, Close, Position
  } from '@element-plus/icons-vue';
  
  // 移动端菜单状态
  const mobileMenuOpen = ref(false);
  const toggleMobileMenu = () => {
    mobileMenuOpen.value = !mobileMenuOpen.value;
  };
  
  // AI 助手状态
  const showAIAssistant = ref(true);
  const toggleAIAssistant = () => {
    showAIAssistant.value = !showAIAssistant.value;
  };
  
  // 未来科技数据
  const futureTechnologies = ref([
    {
      title: '量子通信与加密网络',
      description: '基于量子力学原理的下一代通信技术，提供理论上无法破解的加密方案，为国家级通信系统提供安全保障。',
      image: '/img_4.jpg',
      tags: ['量子纠缠', '密钥分发', '无条件安全']
    },
    {
      title: '脑机接口技术',
      description: '直接连接人脑与计算机的革命性技术，实现思维控制设备、辅助残障人士，并为元宇宙提供全新交互方式。',
      image: '/img_5.jpg',
      tags: ['神经接口', '意念控制', '康复医疗']
    },
    {
      title: '全息投影与空间运算',
      description: '无需穿戴设备的三维全息投影技术，实现空间中的自然交互，广泛应用于教育、建筑、医疗和娱乐领域。',
      image: '/img_27.jpg',
      tags: ['空间计算', '裸眼3D', '交互设计']
    },
    {
      title: '智能材料与仿生机械',
      description: '具有自修复能力的新型材料与柔性机器人技术，模拟生物结构与功能，实现更安全高效的人机协作。',
      image: '/img_26.jpg',
      tags: ['自修复', '柔性机器人', '仿生设计']
    },
    {
      title: '可控核聚变研究',
      description: '模拟太阳能量产生原理的清洁能源技术，结合人工智能优化等离子体控制，有望彻底解决人类能源危机。',
      image: '/img_6.jpg',
      tags: ['清洁能源', '等离子体', '人工太阳']
    },
    {
      title: '通用人工智能系统',
      description: '具备自学习、自推理、自演化能力的新一代AI系统，作为未来智慧城市、企业和国家的智能中枢。',
      image: '/img_14.jpg',
      tags: ['自主学习', '跨域推理', '智能决策']
    },
    {
      title: '太空探索与星链通信',
      description: '构建月球无人基站与小型卫星星链网络，开展超光速通信实验，建立地外同步通信系统。',
      image: '/img_15.jpg',
      tags: ['卫星网络', '月球基站', '深空通信']
    },
    {
      title: '数字孪生城市引擎',
      description: '构建物理世界的高精度数字映射与运算管理系统，为城市管理、公共安全与空间治理提供全新解决方案。',
      image: '/img_1.jpg',
      tags: ['城市建模', '实时监控', '预测分析']
    },
    {
      title: '生物计算与基因编辑',
      description: '结合DNA存储、蛋白质计算与CRISPR技术，开发全新计算范式与精准医疗方案，引领生物技术革命。',
      image: '/img_20.jpg',
      tags: ['DNA存储', '精准医疗', '合成生物学']
    }
  ]);
  
  // 行业解决方案数据
  const selectedSolution = ref(0);
  const industrySolutions = ref([
    {
      title: '智慧城市',
      description: '基于物联网、数字孪生与AI大脑的新一代城市管理系统，实现城市资源的智能调度、公共安全的主动防护与市民服务的精准提供。',
      image: '/img_29.jpg',
      technologies: [
        { name: 'IoT感知网络', description: '覆盖全城的多层次物联网感知系统' },
        { name: '数字孪生平台', description: '城市物理空间的高精度数字映射' },
        { name: 'AI城市大脑', description: '多维数据融合的智能决策系统' },
        { name: '智慧交通调度', description: '基于实时数据的交通流优化系统' }
      ]
    },
    {
      title: '未来医疗',
      description: '融合人工智能诊断、纳米机器人治疗与远程手术平台的医疗技术体系，提供精准、高效、普惠的新一代医疗服务。',
      image: '/img_9.jpg',
      technologies: [
        { name: 'AI辅助诊断', description: '多模态医学影像智能分析系统' },
        { name: '纳米医疗机器人', description: '靶向药物递送与微创治疗技术' },
        { name: '远程手术平台', description: '低延迟高精度远程操作系统' },
        { name: '健康大数据平台', description: '全生命周期健康数据管理系统' }
      ]
    },
    {
      title: '智能制造',
      description: '结合柔性生产线、AI质检系统与协作机器人的新一代制造范式，实现高度自动化、定制化与资源优化的生产模式。',
      image: '/img_24.jpg',
      technologies: [
        { name: '柔性自动化生产线', description: '快速重构的模块化生产系统' },
        { name: 'AI视觉质检系统', description: '亚毫米级缺陷实时检测技术' },
        { name: '协作机器人集群', description: '人机协同的智能作业系统' },
        { name: '数字孪生工厂', description: '生产流程全周期优化平台' }
      ]
    },
    {
      title: '教育与文化',
      description: '通过AI教师、知识脑机接口与非遗数字存档技术，创造沉浸式、个性化、高效率的未来教育体验，同时保护和传承珍贵文化遗产。',
      image: '/img_23.jpg',
      technologies: [
        { name: 'AI个性化教学', description: '自适应学习路径规划系统' },
        { name: '知识脑机接口', description: '直接神经信息传递学习技术' },
        { name: '沉浸式文化体验', description: '多感官全息文化遗产重现系统' },
        { name: '非遗数字化平台', description: '传统技艺高精度捕捉与存档技术' }
      ]
    },
    {
      title: '国家安全',
      description: '基于量子加密、无人防御系统与战略仿真沙盘的综合安全解决方案，为国家关键基础设施与信息系统提供最高级别保护。',
      image: '/img_19.jpg',
      technologies: [
        { name: '量子加密通信', description: '理论上无法破解的信息保护系统' },
        { name: '无人防御系统', description: 'AI驱动的多层次安全防护网络' },
        { name: '战略仿真沙盘', description: '高精度态势感知与决策支持平台' },
        { name: '网络空间防护', description: '关键信息基础设施保护系统' }
      ]
    },
    {
      title: '绿色能源',
      description: '围绕可控核聚变、智能电网与碳中和管理系统，构建清洁、高效、可持续的未来能源体系，助力全球应对气候变化挑战。',
      image: '/img_13.jpg',
      technologies: [
        { name: '可控核聚变反应堆', description: '下一代清洁能源核心技术' },
        { name: '智能电网系统', description: '多源能源高效协同调度平台' },
        { name: '碳中和管理平台', description: '全生命周期碳排放监测与优化系统' },
        { name: '能源存储技术', description: '高密度长寿命新型储能解决方案' }
      ]
    },
    {
      title: '太空经济',
      description: '通过轨道物流、月面资源勘探与空天作战模拟系统，开拓太空经济新疆域，保障国家太空资产安全与资源获取能力。',
      image: '/img_0.jpg',
      technologies: [
        { name: '轨道物流系统', description: '低成本高效率太空运输网络' },
        { name: '月面资源勘探', description: '自主月球基地与资源提取技术' },
        { name: '空天一体化平台', description: '天地一体化指挥控制系统' },
        { name: '卫星互联网络', description: '全球覆盖的高速空间数据网' }
      ]
    }
  ]);
  
  // 研究实验室数据
  const researchLabs = ref([
    {
      name: '量子信息实验室',
      description: '专注于量子通信、量子计算与量子密码学研究，开发下一代信息处理与安全技术。',
      image: '/img_21.jpg',
      researchAreas: ['量子纠缠', '量子计算', '量子密码学']
    },
    {
      name: '脑科学与接口中心',
      description: '研究大脑工作机制与脑机接口技术，开发直接神经信息传输与处理的革命性技术。',
      image: '/img_22.jpg',
      researchAreas: ['神经编码', '脑机接口', '认知增强']
    },
    {
      name: '先进材料研究院',
      description: '开发智能材料、超导体与纳米复合材料，为未来设备与基础设施提供革命性材料基础。',
      image: '/img_11.jpg',
      researchAreas: ['智能材料', '超导技术', '纳米工程']
    },
    {
      name: '能源科学中心',
      description: '致力于可控核聚变、高效储能与能源智能管理系统研究，解决人类可持续能源难题。',
      image: '/img_3.jpg',
      researchAreas: ['核聚变', '储能技术', '智能电网']
    },
    {
      name: '人工智能研究所',
      description: '研发通用人工智能、类脑计算与自主学习系统，推动AI从专用向通用方向发展。',
      image: '/img_17.jpg',
      researchAreas: ['通用AI', '类脑计算', '自主学习']
    },
    {
      name: '空间技术实验室',
      description: '开展太空探索、卫星通信与空间资源利用研究，为人类太空经济发展奠定基础。',
      image: '/img_8.jpg',
      researchAreas: ['卫星技术', '月球基地', '太空资源']
    }
  ]);
  
  // 合作伙伴数据
  const partners = ref([
    { name: '北京大学', icon: 'School' },
    { name: '清华大学', icon: 'School' },
    { name: '中国科学院', icon: 'OfficeBuilding' },
    { name: '麻省理工学院', icon: 'School' },
    { name: '斯坦福大学', icon: 'School' },
    { name: '国家实验室', icon: 'OfficeBuilding' },
    { name: '华为技术', icon: 'Cpu' },
    { name: '阿里巴巴', icon: 'ShoppingCart' },
    { name: '腾讯科技', icon: 'ChatDotRound' },
    { name: '微软研究院', icon: 'Monitor' },
    { name: '谷歌 DeepMind', icon: 'Connection' },
    { name: '特斯拉', icon: 'Lightning' }
  ]);
  
  // 新闻文章数据
  const newsArticles = ref([
    {
      title: 'CiumHoa 量子通信网络实现千公里级安全传输',
      summary: '我们的研究团队成功实现了基于量子纠缠的千公里级安全通信，为构建全国量子保密通信骨干网奠定基础。该技术已在金融、政务等关键领域开始试点应用。',
      category: '技术突破',
      date: '2025-04-18',
      image: '/img_16.jpg'
    },
    {
      title: '脑机接口技术助力高位截瘫患者重获行走能力',
      summary: '我们的脑机接口与外骨骼结合技术成功帮助一位高位截瘫患者恢复基本行走能力，标志着神经修复技术取得重大突破。该系统通过解码大脑运动意图直接控制外骨骼系统。',
      category: '医疗应用',
      date: '2025-04-10',
      image: '/img_10.jpg'
    },
    {
      title: 'CiumHoa 与国家电网合作开发智能电网管理系统',
      summary: '我们与国家电网签署战略合作协议，共同开发新一代智能电网管理系统，整合可再生能源、储能设备与用电负荷，实现电网的高效运行与智能调度。',
      category: '战略合作',
      date: '2025-04-02',
      image: '/img_12.jpg'
    }
  ]);
  
  // 未来科技指数图表
  const techIndexChart = ref<HTMLElement | null>(null);
  let chart: echarts.ECharts | null = null;
  
  onMounted(() => {
    // 初始化粒子效果
    initParticles();
    
    // 初始化图表
    nextTick(() => {
      if (techIndexChart.value) {
        chart = echarts.init(techIndexChart.value);
        
        const option = {
          animation: false,
          tooltip: {
            trigger: 'axis',
            axisPointer: {
              type: 'shadow'
            }
          },
          legend: {
            data: ['研发投入', '技术成熟度', '市场应用'],
            textStyle: {
              color: '#a0aec0'
            }
          },
          grid: {
            left: '3%',
            right: '4%',
            bottom: '3%',
            containLabel: true
          },
          xAxis: {
            type: 'category',
            data: ['量子通信', '脑机接口', '全息投影', '智能材料', '核聚变', '通用AI', '太空技术', '数字孪生'],
            axisLine: {
              lineStyle: {
                color: '#4a5568'
              }
            },
            axisLabel: {
              color: '#a0aec0',
              rotate: 45
            }
          },
          yAxis: {
            type: 'value',
            max: 100,
            axisLine: {
              lineStyle: {
                color: '#4a5568'
              }
            },
            axisLabel: {
              color: '#a0aec0'
            },
            splitLine: {
              lineStyle: {
                color: '#2d3748'
              }
            }
          },
          series: [
            {
              name: '研发投入',
              type: 'bar',
              stack: 'total',
              emphasis: {
                focus: 'series'
              },
              data: [85, 72, 68, 75, 92, 88, 78, 70],
              itemStyle: {
                color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [
                  { offset: 0, color: '#3182ce' },
                  { offset: 1, color: '#2c5282' }
                ])
              }
            },
            {
              name: '技术成熟度',
              type: 'bar',
              stack: 'total',
              emphasis: {
                focus: 'series'
              },
              data: [65, 58, 70, 62, 45, 75, 60, 72],
              itemStyle: {
                color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [
                  { offset: 0, color: '#805ad5' },
                  { offset: 1, color: '#553c9a' }
                ])
              }
            },
            {
              name: '市场应用',
              type: 'bar',
              stack: 'total',
              emphasis: {
                focus: 'series'
              },
              data: [50, 42, 65, 55, 30, 60, 45, 68],
              itemStyle: {
                color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [
                  { offset: 0, color: '#38b2ac' },
                  { offset: 1, color: '#234e52' }
                ])
              }
            }
          ]
        };
        
        chart.setOption(option);
        
        window.addEventListener('resize', () => {
          chart?.resize();
        });
      }
    });
  });
  
  // 粒子效果初始化
  const particlesContainer = ref<HTMLElement | null>(null);
  function initParticles() {
    // 这里仅模拟粒子效果，实际项目中可以使用专门的粒子库
    if (particlesContainer.value) {
      const canvas = document.createElement('canvas');
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
      canvas.style.position = 'absolute';
      canvas.style.top = '0';
      canvas.style.left = '0';
      canvas.style.width = '100%';
      canvas.style.height = '100%';
      particlesContainer.value.appendChild(canvas);
      
      const ctx = canvas.getContext('2d');
      if (!ctx) return;
      
      const particles: { x: number; y: number; size: number; speedX: number; speedY: number; opacity: number }[] = [];
      const particleCount = 100;
      
      // 创建粒子
      for (let i = 0; i < particleCount; i++) {
        particles.push({
          x: Math.random() * canvas.width,
          y: Math.random() * canvas.height,
          size: Math.random() * 2 + 1,
          speedX: (Math.random() - 0.5) * 0.5,
          speedY: (Math.random() - 0.5) * 0.5,
          opacity: Math.random() * 0.5 + 0.2
        });
      }
      
      function drawParticles() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        
        particles.forEach(particle => {
          ctx.beginPath();
          ctx.arc(particle.x, particle.y, particle.size, 0, Math.PI * 2);
          ctx.fillStyle = `rgba(100, 149, 237, ${particle.opacity})`;
          ctx.fill();
          
          // 更新位置
          particle.x += particle.speedX;
          particle.y += particle.speedY;
          
          // 边界检查
          if (particle.x < 0 || particle.x > canvas.width) {
            particle.speedX = -particle.speedX;
          }
          
          if (particle.y < 0 || particle.y > canvas.height) {
            particle.speedY = -particle.speedY;
          }
        });
        
        requestAnimationFrame(drawParticles);
      }
      
      drawParticles();
      
      // 窗口大小变化时调整画布大小
      window.addEventListener('resize', () => {
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
      });
    }
  }
  </script>
  
  <style scoped>
  /* 自定义样式 */
  .ciumhoa-gradient-text {
    background: linear-gradient(90deg, #3182ce, #805ad5);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
  }
  
  /* 滚动条样式 */
  ::-webkit-scrollbar {
    width: 8px;
    height: 8px;
  }
  
  ::-webkit-scrollbar-track {
    background: #1a202c;
  }
  
  ::-webkit-scrollbar-thumb {
    background: #4a5568;
    border-radius: 4px;
  }
  
  ::-webkit-scrollbar-thumb:hover {
    background: #3182ce;
  }
  
  /* 移除number输入框的箭头 */
  input[type="number"]::-webkit-inner-spin-button,
  input[type="number"]::-webkit-outer-spin-button {
    -webkit-appearance: none;
    margin: 0;
  }
  
  input[type="number"] {
    -moz-appearance: textfield;
  }
  
  /* 选择框样式 */
  select {
    appearance: none;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='/img_7.jpg' fill='none' viewBox='0 0 24 24' stroke='%234a5568'%3E%3Cpath stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M19 9l-7 7-7-7'%3E%3C/path%3E%3C/svg%3E");
    background-repeat: no-repeat;
    background-position: right 0.75rem center;
    background-size: 1rem;
    padding-right: 2.5rem;
  }
  </style>
  
  