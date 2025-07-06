<template>
  <div class="min-h-screen bg-gradient-to-br from-gray-900 via-black to-purple-900 relative overflow-hidden">
    <!-- Background Effects -->
    <div class="absolute inset-0 bg-black"></div>

    <!-- Linha Horizontal Superior -->
    <div class="line-wrapper horizontal top">
      <div class="line horizontal-line">
        <div class="line-glow"></div>
        <div class="line-core"></div>
        <div class="animated-dot dot-1"></div>
      </div>
    </div>

    <!-- Linha Vertical Esquerda -->
    <div class="line-wrapper vertical left">
      <div class="line vertical-line">
        <div class="line-glow"></div>
        <div class="line-core"></div>
        <div class="animated-dot dot-2"></div>
      </div>
    </div>

    <!-- Linha Diagonal -->
    <div class="line-wrapper diagonal">
      <div class="line diagonal-line">
        <div class="line-glow"></div>
        <div class="line-core"></div>
        <div class="animated-dot dot-3"></div>
      </div>
    </div>

    <!-- Linha Vertical Direita -->
    <div class="line-wrapper vertical right">
      <div class="line vertical-line">
        <div class="line-glow"></div>
        <div class="line-core"></div>
        <div class="animated-dot dot-4"></div>
      </div>
    </div>

    <!-- Linha Horizontal Inferior -->
    <div class="line-wrapper horizontal bottom">
      <div class="line horizontal-line">
        <div class="line-glow"></div>
        <div class="line-core"></div>
        <div class="animated-dot dot-5"></div>
      </div>
    </div>

    <!-- Linha Curva -->
    <div class="line-wrapper curved">
      <svg class="curved-line" viewBox="0 0 200 100">
        <defs>
          <linearGradient id="curvedGradient" x1="0%" y1="0%" x2="100%" y2="0%">
            <stop offset="0%" style="stop-color:#ec4899;stop-opacity:0" />
            <stop offset="50%" style="stop-color:#ec4899;stop-opacity:1" />
            <stop offset="100%" style="stop-color:#ef4444;stop-opacity:0" />
          </linearGradient>
        </defs>
        <path
          d="M 10 50 Q 100 10 190 50"
          stroke="url(#curvedGradient)"
          stroke-width="2"
          fill="none"
          class="animated-path"
        />
      </svg>
    </div>

    <!-- Linhas de Grid Animadas -->
    <div class="grid-lines">
      <div class="grid-line grid-1"></div>
      <div class="grid-line grid-2"></div>
      <div class="grid-line grid-3"></div>
      <div class="grid-line grid-4"></div>
    </div>

    <!-- Pulsos de Energia -->
    <div class="energy-pulses">
      <div class="pulse pulse-1"></div>
      <div class="pulse pulse-2"></div>
      <div class="pulse pulse-3"></div>
    </div>
    
    <!-- Floating Pink Elements -->
    <div class="absolute top-32 left-0 w-[900px] h-[1000px] bg-gradient-to-br from-pink-500/20 to-purple-600/10 rounded-full blur-3xl"></div>
    <div class="absolute bottom-20 right-20 w-[500px] h-[800px] bg-pink-500/10 rounded-full blur-2xl"></div>
    
    <!-- Navigation -->
    <nav class="relative z-50 flex justify-between items-center px-8 py-6">
      <div class="flex items-center space-x-2">
        <div class="w-8 h-8 bg-gradient-to-r from-pink-500 to-red-500 rounded-full flex items-center justify-center">
          <span class="text-white font-bold text-sm">C</span>
        </div>
        <span class="text-white text-xl font-bold">Creative</span>
      </div>
      
      <div class="hidden md:flex space-x-8 text-sm">
        <a href="#home" class="text-white hover:text-pink-400 transition-colors font-medium">Home</a>
        <a href="#about" class="text-white hover:text-pink-400 transition-colors font-medium">About</a>
        <div class="relative group">
          <a href="#services" class="text-white hover:text-pink-400 transition-colors font-medium flex items-center">
            Services <ChevronDown class="w-3 h-3 ml-1" />
          </a>
        </div>
        <div class="relative group">
          <a href="#blog" class="text-white hover:text-pink-400 transition-colors font-medium flex items-center">
            Blog <ChevronDown class="w-3 h-3 ml-1" />
          </a>
        </div>
        <div class="relative group">
          <a href="#project" class="text-white hover:text-pink-400 transition-colors font-medium flex items-center">
            Project <ChevronDown class="w-3 h-3 ml-1" />
          </a>
        </div>
        <a href="#contact" class="text-white hover:text-pink-400 transition-colors font-medium">Contact</a>
      </div>
      
      <div class="flex space-x-4">
        <a href="#" class="text-white hover:text-pink-400 transition-colors">
          <Instagram class="w-5 h-5" />
        </a>
        <a href="#" class="text-white hover:text-pink-400 transition-colors">
          <Linkedin class="w-5 h-5" />
        </a>
        <a href="#" class="text-white hover:text-pink-400 transition-colors">
          <Twitter class="w-5 h-5" />
        </a>
        <a href="#" class="text-white hover:text-pink-400 transition-colors">
          <Facebook class="w-5 h-5" />
        </a>
      </div>
      
      <button class="md:hidden text-white p-2 rounded-lg bg-pink-500">
        <Menu class="w-6 h-6" />
      </button>
    </nav>

    <img 
      :src="bgdownImage" 
      alt="bg-down" 
      class="w-full h-full top-2/3 left-2/2 transform -translate-x-1/5 -translate-y-1/2 absolute"
    />
    
    <!-- Main Content -->
    <div class="relative flex flex-col lg:flex-row items-center justify-between px-8 py-12 max-w-7xl mx-auto min-h-[80vh]">
      <!-- Left Content -->
      <div class="flex-1 space-y-6 lg:pr-16" v-motion-slide-visible-once-left>
        <div class="space-y-4">
          <BlurReveal
            :delay="0.5"
            :duration="1.0"
            class=""
          >
            <p class="text-pink-400 text-sm font-medium tracking-widest uppercase">I AM</p>
            <h1 class="text-4xl lg:text-6xl xl:text-7xl font-bold text-white leading-tight">
              Ralph Edwards, a Full Stack
              <br>
              <span class="gradient-text">Content Writer</span>
            </h1>
          </BlurReveal>
        </div>
        
        <div class="space-y-4 text-gray-300 text-base leading-relaxed max-w-xl">
          <p>
            A personal <span class="text-pink-400 font-semibold">portfolio</span> is a collection of your work, that is achievements, and skills that highlights in your abilities and professional 
            <span class="text-pink-400 font-semibold">web design</span> growth. It serves as
          </p>
        </div>
        
        <div class="pt-4">
          <button class="bg-gradient-to-r from-pink-500 to-red-500 text-white px-6 py-3 rounded-full font-medium hover:shadow-lg hover:shadow-pink-500/25 transition-all duration-300 hover:scale-105 flex items-center space-x-2">
            <span>More About Us</span>
            <ChevronRight class="w-4 h-4" />
          </button>
        </div>

        <img 
          :src="bannerImage" 
          alt="raio de luz" 
          class="w-[900px] h-[1500px] top-1/4 left-2/2 transform -translate-x-2/3 -translate-y-3/4 absolute -z-10"
        />
        
        <div class="flex items-center space-x-6 pt-8">
          <p class="text-gray-400 text-sm">Find me on</p>
          <div class="flex space-x-4">
            <a href="#" class="text-gray-400 hover:text-pink-400 transition-colors p-2 rounded-full hover:bg-white/5">
              <Instagram class="w-4 h-4" />
            </a>
            <a href="#" class="text-gray-400 hover:text-pink-400 transition-colors p-2 rounded-full hover:bg-white/5">
              <Linkedin class="w-4 h-4" />
            </a>
            <a href="#" class="text-gray-400 hover:text-pink-400 transition-colors p-2 rounded-full hover:bg-white/5">
              <Twitter class="w-4 h-4" />
            </a>
            <a href="#" class="text-gray-400 hover:text-pink-400 transition-colors p-2 rounded-full hover:bg-white/5">
              <Facebook class="w-4 h-4" />
            </a>
          </div>
        </div>
      </div>

        <!-- Floating Pink Elements -->
        <div class="absolute top-4/4 left-2/4 w-[700px] h-[800px] bg-pink-900/30 rounded-full blur-3xl"></div>
        <div class="absolute top-2/4 left-2/4 w-[700px] h-[700px] bg-black/80 rounded-full blur-3xl z-10"></div>
        <div class="absolute top-3/4 right-1/2 w-[900px] h-[700px] bg-black/80 rounded-full blur-3xl"></div>

        <img 
          :src="bannerImage" 
          alt="raio de luz" 
          class="w-[900px] h-[1200px] top-3/3 left-2/4 transform -translate-x-1/2 -translate-y-1/2 absolute z-20"
        />

      <!-- Right Content - Profile Image -->
      <div class="flex-1 flex justify-center items-center relative mt-12 lg:mt-0" v-motion-slide-visible-once-right>
        <div class="relative">
          <!-- Large Pink Circle Background -->
          <div class="absolute -top-0 -right-20 w-[550px] h-[550px] bg-gradient-to-br from-pink-500/5 to-purple-600/5 rounded-full z-0"></div>
          
          <!-- Novo texto "UX Designer" atrás da imagem -->
          <div class="absolute top-1/3 left-2/4 transform -translate-x-1/2 -translate-y-1/2 pointer-events-none z-0">
            <BlurReveal
              :delay="0.4"
              :duration="0.8"
              class=""
            >
              <h2 class="text-6xl lg:text-8xl font-bold text-white tracking-wider whitespace-nowrap animate-float">
                UX Designer
              </h2>
            </BlurReveal>
          </div>
          
          <img 
            :src="timeImage" 
            alt="time" 
            class="w-[550px] h-[450px] object-cover absolute z-20 top-1/3 left-1/3 animate-rotate"
          />
          
          <!-- Imagem Hero -->
          <img 
            :src="profileImage" 
            alt="JSF" 
            class="w-full h-full object-cover relative z-20"
          />
          <NeonBorder :animation-type="'full'"></NeonBorder>
       
          <!-- Texto "UX Designer" flutuante na frente -->
          <div class="absolute top-3/4 left-2/3 transform -translate-x-1/3 -translate-y-3/4 pointer-events-none z-10">
            <h2 class="text-6xl lg:text-8xl font-bold text-white/80 tracking-wider whitespace-nowrap animate-float">
              UX Designer
            </h2>
          </div>

          <!-- Circular Skills Indicator -->
          <div class="absolute top-0 left-3/2 transform -translate-x-1/2 z-20">
            <div class="relative w-20 h-20 bg-black/10 rounded-full flex items-center justify-center backdrop-blur-sm">
              <!-- Outer Ring -->
              <svg class="absolute w-full h-full transform -rotate-90" viewBox="0 0 100 100">
                <circle
                  cx="50"
                  cy="50"
                  r="45"
                  stroke="rgba(255,255,255,0.1)"
                  stroke-width="2"
                  fill="none"
                />
                <circle
                  cx="50"
                  cy="50"
                  r="45"
                  stroke="url(#gradient)"
                  stroke-width="2"
                  fill="none"
                  stroke-linecap="round"
                  stroke-dasharray="283"
                  stroke-dashoffset="70"
                />
                <defs>
                  <linearGradient id="gradient" x1="0%" y1="0%" x2="100%" y2="100%">
                    <stop offset="0%" style="stop-color:#ec4899;stop-opacity:1" />
                    <stop offset="100%" style="stop-color:#ef4444;stop-opacity:1" />
                  </linearGradient>
                </defs>
              </svg>
              
              <!-- Center Content -->
              <div class="relative text-center">
                <div class="text-white text-xs font-medium">BEST</div>
                <div class="text-white text-xs font-medium">SWIFT</div>
                <div class="text-white text-xs">Work</div>
              </div>
              
              <!-- Small dots around the circle -->
              <div class="absolute top-2 left-1/2 transform -translate-x-1/2 w-1 h-1 bg-pink-500 rounded-full"></div>
              <div class="absolute bottom-2 left-1/2 transform -translate-x-1/2 w-1 h-1 bg-pink-500 rounded-full"></div>
              <div class="absolute left-2 top-1/2 transform -translate-y-1/2 w-1 h-1 bg-pink-500 rounded-full"></div>
              <div class="absolute right-2 top-1/2 transform -translate-y-1/2 w-1 h-1 bg-pink-500 rounded-full"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
    
    <!-- Scroll Indicator -->
    <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce z-20">
      <ChevronDown class="w-6 h-6 text-white/50" />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { ChevronDown, ChevronRight, Instagram, Linkedin, Twitter, Facebook, Menu } from 'lucide-vue-next'
import BlurReveal from './ui/blur-reveal/BlurReveal.vue';
import { onMounted, onUnmounted } from 'vue'

const profileImage = ref('/hero.png')
const timeImage = ref('/time.png')
const bannerImage = ref('/banner_star_mb.png')
const bgdownImage = ref('/bg-down2.png')
import NeonBorder from "@/components/ui/neon-border/NeonBorder.vue";

// Adicionar efeitos de mouse interativo
const handleMouseMove = (e: MouseEvent) => {
  const lines = document.querySelectorAll('.line')
  const mouseX = e.clientX / window.innerWidth
  const mouseY = e.clientY / window.innerHeight
  
  lines.forEach((line, index) => {
    const element = line as HTMLElement
    const intensity = (mouseX + mouseY) * 0.5
    element.style.setProperty('--mouse-intensity', intensity.toString())
  })
}

onMounted(() => {
  window.addEventListener('mousemove', handleMouseMove, { passive: true })
})

onUnmounted(() => {
  window.removeEventListener('mousemove', handleMouseMove)
})

</script>

<style scoped>

.bg-mesh {
  background-image: 
    radial-gradient(circle at 20% 20%, rgba(236, 72, 153, 0.1) 0%, transparent 50%),
    radial-gradient(circle at 80% 80%, rgba(239, 68, 68, 0.1) 0%, transparent 50%),
    radial-gradient(circle at 40% 40%, rgba(168, 85, 247, 0.1) 0%, transparent 50%);
}

.gradient-text {
  background: linear-gradient(135deg, #ec4899 0%, #ef4444 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.glass {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
}

@keyframes rotate {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

.animate-rotate {
  animation: rotate 10s linear infinite;
}

.animated-lines-container {
  position: relative;
  width: 100%;
  height: 100vh;
  background: radial-gradient(circle at 20% 0%, rgba(236, 72, 153, 0.1) 0%, transparent 50%),
              radial-gradient(circle at 80% 50%, rgba(239, 68, 68, 0.1) 0%, transparent 50%);
  overflow: hidden;
}

.line-wrapper {
  position: absolute;
  z-index: 1;
}

.line {
  position: relative;
  --mouse-intensity: 0.5;
}

.line-glow {
  position: absolute;
  background: linear-gradient(90deg, 
    transparent 0%, 
    rgba(236, 72, 153, 0.3) 20%, 
    rgba(236, 72, 153, 0.8) 50%, 
    rgba(239, 68, 68, 0.8) 50%, 
    rgba(239, 68, 68, 0.3) 80%, 
    transparent 100%);
  filter: blur(4px);
  animation: pulse-glow 3s ease-in-out infinite;
}

.line-core {
  position: absolute;
  background: linear-gradient(90deg, 
    transparent 0%, 
    rgba(236, 72, 153, 0.6) 20%, 
    rgba(236, 72, 153, 1) 50%, 
    rgba(239, 68, 68, 1) 50%, 
    rgba(239, 68, 68, 0.6) 80%, 
    transparent 100%);
  animation: flowing-energy 4s linear infinite;
}

/* Linhas Horizontais */
.horizontal {
  width: 100%;
  height: 2px;
}

.horizontal.top {
  top: 20%;
  left: 0;
}

.horizontal.bottom {
  bottom: 20%;
  left: 0;
}

.horizontal-line .line-glow,
.horizontal-line .line-core {
  width: 100%;
  height: 100%;
}

/* Linhas Verticais */
.vertical {
  width: 2px;
  height: 100%;
}

.vertical.left {
  left: 10%;
  top: 0;
}

.vertical.right {
  right: 10%;
  top: 0;
}

.vertical-line .line-glow,
.vertical-line .line-core {
  width: 100%;
  height: 100%;
  background: linear-gradient(180deg, 
    transparent 0%, 
    rgba(236, 72, 153, 0.3) 20%, 
    rgba(236, 72, 153, 0.8) 50%, 
    rgba(239, 68, 68, 0.8) 50%, 
    rgba(239, 68, 68, 0.3) 80%, 
    transparent 100%);
}

.vertical-line .line-core {
  background: linear-gradient(180deg, 
    transparent 0%, 
    rgba(236, 72, 153, 0.6) 20%, 
    rgba(236, 72, 153, 1) 50%, 
    rgba(239, 68, 68, 1) 50%, 
    rgba(239, 68, 68, 0.6) 80%, 
    transparent 100%);
}

/* Linha Diagonal */
.diagonal {
  top: 10%;
  left: 30%;
  width: 200px;
  height: 2px;
  transform: rotate(45deg);
}

.diagonal-line .line-glow,
.diagonal-line .line-core {
  width: 100%;
  height: 100%;
}

/* Linha Curva */
.curved {
  top: 60%;
  left: 50%;
  transform: translateX(-50%);
  width: 200px;
  height: 100px;
}

.curved-line {
  width: 100%;
  height: 100%;
}

.animated-path {
  stroke-dasharray: 200;
  stroke-dashoffset: 200;
  animation: draw-path 4s ease-in-out infinite;
}

/* Pontos Animados */
.animated-dot {
  position: absolute;
  width: 8px;
  height: 8px;
  background: radial-gradient(circle, rgba(236, 72, 153, 1) 0%, rgba(239, 68, 68, 1) 100%);
  border-radius: 50%;
  box-shadow: 0 0 20px rgba(236, 72, 153, 0.8);
  animation: dot-travel 6s linear infinite;
}

.dot-1 {
  animation-delay: 0s;
}

.dot-2 {
  animation-delay: 1.2s;
}

.dot-3 {
  animation-delay: 2.4s;
}

.dot-4 {
  animation-delay: 3.6s;
}

.dot-5 {
  animation-delay: 4.8s;
}

/* Linhas de Grid */
.grid-lines {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: 0.3;
}

.grid-line {
  position: absolute;
  background: linear-gradient(90deg, 
    transparent 0%, 
    rgba(236, 72, 153, 0.2) 50%, 
    transparent 100%);
  animation: grid-flow 8s linear infinite;
}

.grid-1 {
  top: 25%;
  left: 0;
  width: 100%;
  height: 1px;
  animation-delay: 0s;
}

.grid-2 {
  top: 50%;
  left: 0;
  width: 100%;
  height: 1px;
  animation-delay: 2s;
}

.grid-3 {
  top: 0;
  left: 25%;
  width: 1px;
  height: 100%;
  background: linear-gradient(180deg, 
    transparent 0%, 
    rgba(236, 72, 153, 0.2) 50%, 
    transparent 100%);
  animation-delay: 4s;
}

.grid-4 {
  top: 0;
  left: 75%;
  width: 1px;
  height: 100%;
  background: linear-gradient(180deg, 
    transparent 0%, 
    rgba(236, 72, 153, 0.2) 50%, 
    transparent 100%);
  animation-delay: 6s;
}

/* Pulsos de Energia */
.energy-pulses {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
}

.pulse {
  position: absolute;
  width: 4px;
  height: 4px;
  background: radial-gradient(circle, rgba(236, 72, 153, 1) 0%, transparent 70%);
  border-radius: 50%;
  animation: energy-pulse 5s ease-in-out infinite;
}

.pulse-1 {
  top: 30%;
  left: 20%;
  animation-delay: 0s;
}

.pulse-2 {
  top: 70%;
  left: 80%;
  animation-delay: 1.5s;
}

.pulse-3 {
  top: 50%;
  left: 60%;
  animation-delay: 3s;
}

/* Animações */
@keyframes flowing-energy {
  0% {
    background-position: -100% 0;
  }
  100% {
    background-position: 100% 0;
  }
}

@keyframes pulse-glow {
  0%, 100% {
    opacity: 0.4;
    filter: blur(4px);
  }
  50% {
    opacity: 1;
    filter: blur(2px);
  }
}

@keyframes dot-travel {
  0% {
    transform: translateX(0) translateY(0);
    opacity: 0;
  }
  10% {
    opacity: 1;
  }
  90% {
    opacity: 1;
  }
  100% {
    transform: translateX(400px) translateY(0);
    opacity: 0;
  }
}

@keyframes draw-path {
  0% {
    stroke-dashoffset: 200;
    opacity: 0;
  }
  20% {
    opacity: 1;
  }
  80% {
    opacity: 1;
  }
  100% {
    stroke-dashoffset: -200;
    opacity: 0;
  }
}

@keyframes grid-flow {
  0% {
    transform: scaleX(0);
    opacity: 0;
  }
  50% {
    transform: scaleX(1);
    opacity: 1;
  }
  100% {
    transform: scaleX(0);
    opacity: 0;
  }
}

@keyframes energy-pulse {
  0%, 100% {
    transform: scale(1);
    opacity: 1;
  }
  50% {
    transform: scale(3);
    opacity: 0.3;
  }
}

/* Efeitos de Hover e Interatividade */
.line:hover .line-glow {
  filter: blur(2px);
  opacity: 1;
}

.line:hover .line-core {
  animation-duration: 2s;
}

/* Responsividade */
@media (max-width: 768px) {
  .diagonal {
    width: 100px;
  }
  
  .curved {
    width: 150px;
    height: 75px;
  }
  
  .animated-dot {
    width: 6px;
    height: 6px;
  }
}

.line {
  transition: all 0.3s ease;
}

.line:hover {
  transform: scale(1.05);
}

</style>