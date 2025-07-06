<template>
  <div 
    class="scrollToTop" 
    :class="{ 'active-progress': isVisible }"
    :style="{ display: isVisible ? 'block' : 'none' }"
    @click="scrollToTop"
  >
    <div class="arrowUp">
      <!-- Seta SVG como fallback -->
      <svg 
        width="20" 
        height="20" 
        viewBox="0 0 24 24" 
        fill="none" 
        stroke="currentColor" 
        stroke-width="2" 
        stroke-linecap="round" 
        stroke-linejoin="round"
      >
        <path d="M18 15l-6-6-6 6"/>
      </svg>
    </div>
    <div class="water" :style="{ transform: `translate(0px, ${waterLevel}%)` }">
      <svg viewBox="0 0 560 20" class="water_wave water_wave_back">
        <use xlink:href="#wave"></use>
      </svg>
      <svg viewBox="0 0 560 20" class="water_wave water_wave_front">
        <use xlink:href="#wave"></use>
      </svg>
      <svg 
        version="1.1" 
        xmlns="http://www.w3.org/2000/svg" 
        xmlns:xlink="http://www.w3.org/1999/xlink" 
        viewBox="0 0 560 20" 
        style="display: none;"
      >
        <symbol id="wave">
          <path 
            d="M420,20c21.5-0.4,38.8-2.5,51.1-4.5c13.4-2.2,26.5-5.2,27.3-5.4C514,6.5,518,4.7,528.5,2.7c7.1-1.3,17.9-2.8,31.5-2.7c0,0,0,0,0,0v20H420z" 
            fill="#ec4899"
            :style="{ 
              transition: 'stroke-dashoffset 10ms linear', 
              strokeDasharray: '301.839, 301.839', 
              strokeDashoffset: `${dashOffset}px` 
            }"
          />
          <path 
            d="M420,20c-21.5-0.4-38.8-2.5-51.1-4.5c-13.4-2.2-26.5-5.2-27.3-5.4C326,6.5,322,4.7,311.5,2.7C304.3,1.4,293.6-0.1,280,0c0,0,0,0,0,0v20H420z" 
            fill="#ec4899"
          />
          <path 
            d="M140,20c21.5-0.4,38.8-2.5,51.1-4.5c13.4-2.2,26.5-5.2,27.3-5.4C234,6.5,238,4.7,248.5,2.7c7.1-1.3,17.9-2.8,31.5-2.7c0,0,0,0,0,0v20H140z" 
            fill="#ec4899"
          />
          <path 
            d="M140,20c-21.5-0.4-38.8-2.5-51.1-4.5c-13.4-2.2-26.5-5.2-27.3-5.4C46,6.5,42,4.7,31.5,2.7C24.3,1.4,13.6-0.1,0,0c0,0,0,0,0,0l0,20H140z" 
            fill="#ec4899"
          />
        </symbol>
      </svg>
    </div>
  </div>
</template>

<script>
import { ref, onMounted, onUnmounted } from 'vue'

export default {
  name: 'ScrollToTop',
  setup() {
    const isVisible = ref(false)
    const scrollProgress = ref(0)
    const waterLevel = ref(100)
    const dashOffset = ref(45.1414)

    const handleScroll = () => {
      const scrollTop = window.pageYOffset || document.documentElement.scrollTop
      const scrollHeight = document.documentElement.scrollHeight - window.innerHeight
      const progress = (scrollTop / scrollHeight) * 100
      
      // Mostrar botão após 20% do scroll
      isVisible.value = scrollTop > 300
      
      // Calcular progresso do scroll
      scrollProgress.value = progress
      
      // Animar o nível da água baseado no progresso
      waterLevel.value = Math.max(15, 100 - progress)
      
      // Animar o stroke-dashoffset
      dashOffset.value = 301.839 - (progress / 100) * 301.839
    }

    const scrollToTop = () => {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      })
    }

    onMounted(() => {
      window.addEventListener('scroll', handleScroll)
      handleScroll()
    })

    onUnmounted(() => {
      window.removeEventListener('scroll', handleScroll)
    })

    return {
      isVisible,
      scrollProgress,
      waterLevel,
      dashOffset,
      scrollToTop
    }
  }
}
</script>

<style scoped>
.scrollToTop {
  position: fixed;
  bottom: 30px;
  right: 30px;
  width: 60px;
  height: 60px;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border: 2px solid rgba(236, 72, 153, 0.3);
  border-radius: 50%;
  cursor: pointer;
  transition: all 0.3s ease;
  z-index: 1000;
  overflow: hidden;
  opacity: 0;
  transform: translateY(20px);
}

.scrollToTop.active-progress {
  opacity: 1;
  transform: translateY(0);
}

.scrollToTop:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(236, 72, 153, 0.3);
  border-color: rgba(236, 72, 153, 0.6);
}

.arrowUp {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 2;
  color: white;
  font-size: 20px;
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;
}

.arrowUp svg {
  width: 24px;
  height: 24px;
  stroke: currentColor;
  transition: all 0.3s ease;
}

.scrollToTop:hover .arrowUp {
  transform: translate(-50%, -50%) translateY(-2px);
  color: #ec4899;
}

.scrollToTop:hover .arrowUp svg {
  stroke: #ec4899;
  transform: scale(1.1);
}

.water {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100%;
  transition: transform 0.3s ease;
  z-index: 0;
}

.water_wave {
  position: absolute;
  width: 100%;
  height: 100%;
  bottom: 0;
  left: 0;
}

.water_wave_back {
  animation: wave-back 3s ease-in-out infinite;
  opacity: 0.6;
}

.water_wave_front {
  animation: wave-front 2s ease-in-out infinite;
  opacity: 0.8;
}

@keyframes wave-back {
  0%, 100% { transform: translateX(0); }
  50% { transform: translateX(-10px); }
}

@keyframes wave-front {
  0%, 100% { transform: translateX(0); }
  50% { transform: translateX(10px); }
}

.scrollToTop:hover .water_wave {
  animation-duration: 1.5s;
}

@media (max-width: 768px) {
  .scrollToTop {
    bottom: 20px;
    right: 20px;
    width: 50px;
    height: 50px;
  }
  
  .arrowUp svg {
    width: 20px;
    height: 20px;
  }
}

.scrollToTop {
  animation: fadeInUp 0.5s ease-out;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.scrollToTop::before {
  content: '';
  position: absolute;
  top: -2px;
  left: -2px;
  right: -2px;
  bottom: -2px;
  background: linear-gradient(45deg, #ec4899, #ef4444, #8b5cf6, #06b6d4, #ec4899);
  background-size: 200% 200%;
  animation: gradient-border 3s linear infinite;
  border-radius: 50%;
  z-index: -1;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.scrollToTop:hover::before {
  opacity: 1;
}

@keyframes gradient-border {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}
</style>