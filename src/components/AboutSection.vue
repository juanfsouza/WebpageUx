<template>
  <div class="min-h-screen bg-gradient-to-br from-gray-900 via-black to-purple-900 text-white relative overflow-hidden">
    <div class="absolute top-1/5 right-2/3 w-[1000px] h-[500px] bg-black/80 rounded-full blur-3xl z-10"></div>
    <div class="absolute top-1/5 left-2/3 w-[1000px] h-[500px] bg-black/80 rounded-full blur-3xl z-10"></div>
    <div class="absolute inset-0 bg-black"></div>
  
    <!-- Animated Background -->
    <div class="absolute inset-0 bg-mesh bg-pattern opacity-80"></div>
    
    <!-- Floating Background Elements -->
    <div class="absolute top-20 left-10 w-96 h-96 bg-gradient-to-br from-pink-500/20 to-purple-600/10 rounded-full blur-3xl floating-element"></div>
    <div class="absolute bottom-20 right-10 w-[400px] h-[400px] bg-gradient-to-br from-red-500/20 to-pink-600/10 rounded-full blur-3xl floating-element" style="animation-delay: -5s;"></div>
    <div class="absolute top-1/2 left-1/4 w-64 h-64 bg-gradient-to-br from-blue-500/10 to-purple-600/10 rounded-full blur-3xl floating-element" style="animation-delay: -4s;"></div>
    
      <!-- Main Content -->
    <div class="relative z-0 py-20 px-6">
      <div class="max-w-7xl mx-auto">
      <!-- Hero Text Section -->
      <div class="mb-20 relative z-10">
        <div class="max-w-6xl mx-auto text-center">
          <BlurReveal :delay="0.5" :duration="2.0" :blur="'20px'" :yOffset="50">
            <p class="text-2xl md:text-4xl lg:text-5xl font-bold leading-tight text-gray-300 text-shadow">
              A personal
              <span class="gradient-text"> portfolio </span>
              is a collection of your work, that is
              <span class="text-gray-500"> achievements</span>, and skills that highlights
              <span class="gradient-text"> web design </span>
              in your abilities and
              <span class="text-gray-500"> professional growth</span>. It serves as a personal
              <span class="text-gray-500"> portfolio </span>
              in
              <span class="gradient-text"> since 2009 </span>
              a collection of your work
            </p>
          </BlurReveal>
        </div>
      </div>
      
        <img 
          :src="aboutheroImage" 
          alt="about-hero" 
          class=" top-2/4 left-1/5 transform -translate-x-1/4 -translate-y-1/3 absolute md:block hidden sway -z-20 opacity-40"
        />

        <!-- Main About Section -->
        <div class="grid lg:grid-cols-2 gap-16 items-center">
          <!-- Left Side - Experience Circle -->
          <div class="relative flex justify-center scroll-reveal" :class="{ 'revealed': isVisible.experience }" data-section="experience">
            <div class="relative perspective-card">
              <!-- Large gradient circle background -->
              <div class="absolute inset-0 w-96 h-96 bg-gradient-to-br from-pink-500/30 via-red-500/30 to-purple-600/20 rounded-full blur-3xl pulse-glow"></div>
              
              <!-- Main circle with neon border -->
              <div class="relative w-80 h-80 rounded-full gradient-bg flex items-center justify-center neon-border card-3d hover-lift">
                <div class="text-center relative z-10">
                  <div class="text-6xl font-bold text-white mb-2 text-shadow">10+</div>
                  <div class="text-2xl font-semibold text-white">Years Of</div>
                  <div class="text-2xl font-semibold text-white">Experience</div>
                </div>
              </div>

              <!-- UI/UX Design Badge -->
              <div class="absolute -bottom-8 left-1/2 transform -translate-x-1/2 glass-effect rounded-full px-6 py-4 neon-border hover-lift">
                <div class="flex items-center space-x-3">
                  <div class="w-8 h-8 gradient-bg rounded-full flex items-center justify-center">
                    <svg class="w-4 h-4 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2-2v2m8 0V6a2 2 0 012 2v6a2 2 0 01-2 2H6a2 2 0 01-2-2V8a2 2 0 012-2V6"></path>
                    </svg>
                  </div>
                  <div>
                    <div class="text-white font-semibold">UI/UX Design</div>
                    <div class="text-gray-300 text-sm">241 Projects</div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Right Side - About Content -->
          <div class="space-y-8 scroll-reveal" :class="{ 'revealed': isVisible.content }" data-section="content">
            <div>
              <BlurReveal :delay="0.5" :duration="2.0" :blur="'20px'" :yOffset="50">
              <div class="text-pink-500 font-semibold text-sm tracking-wider uppercase mb-4">
                ABOUT ME
              </div>
              <h2 class="text-4xl lg:text-5xl font-bold text-white mb-6 leading-tight text-shadow">
                Boost Business Strategic
                <br>
                Solutions with Us
              </h2>
              <p class="text-gray-300 text-lg leading-relaxed">
                Business consulting consultants provide expert advice and guide businesses to
                help them improve their performance, efficiency, and organizational
              </p>
              </BlurReveal>
            </div>
            
            <!-- Service Cards -->
            <div class="grid md:grid-cols-2 gap-6">
              <div class="glass-effect rounded-2xl p-6 hover-lift card-3d transition-all duration-300 group cursor-pointer">
                <div class="flex items-center space-x-3 mb-4">
                  <div class="w-12 h-12 gradient-bg rounded-full flex items-center justify-center group-hover:scale-110 transition-transform duration-300">
                    <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"></path>
                    </svg>
                  </div>
                  <BlurReveal :delay="0.5" :duration="2.0" :blur="'20px'" :yOffset="50">
                  <h3 class="text-white font-semibold text-lg">Business Solutions</h3>
                  </BlurReveal>
                </div>
                <BlurReveal :delay="0.5" :duration="2.0" :blur="'20px'" :yOffset="50">
                <p class="text-gray-300 text-sm">
                  Each one showcases my approach and dedication to detail, creativity
                </p>
                </BlurReveal>
              </div>

              <div class="glass-effect rounded-2xl p-6 hover-lift card-3d transition-all duration-300 group cursor-pointer">
                <div class="flex items-center space-x-3 mb-4">
                  <div class="w-12 h-12 gradient-bg rounded-full flex items-center justify-center group-hover:scale-110 transition-transform duration-300">
                    <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"></path>
                    </svg>
                  </div>
                  <BlurReveal :delay="0.5" :duration="2.0" :blur="'20px'" :yOffset="50">
                  <h3 class="text-white font-semibold text-lg">Profit Partners</h3>
                  </BlurReveal>
                </div>
                <BlurReveal :delay="0.5" :duration="2.0" :blur="'20px'" :yOffset="50">
                <p class="text-gray-300 text-sm">
                  Business consulting consul us to a provide expert advice businesses
                </p>
                </BlurReveal>
              </div>
            </div>

            <!-- CTA Button -->
            <div class="pt-6">
              <BlurReveal :delay="0.5" :duration="2.0" :blur="'20px'" :yOffset="50">
                <button class="gradient-bg text-white px-8 py-4 rounded-full font-semibold text-lg hover:shadow-lg hover:shadow-pink-500/25 transition-all duration-300 hover:scale-105 flex items-center space-x-2 group neon-border">
                  <span>Read More About Me</span>
                  <svg class="w-5 h-5 group-hover:translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
                  </svg>
                </button>
              </BlurReveal>
            </div>
          </div>
        </div>
        
        <div class="absolute top-3/4 right-2/4 w-[1000px] h-[500px] bg-black rounded-full blur-3xl z-0"></div>

        <!-- Stats Section -->
        <div class="mt-20 grid grid-cols-2 md:grid-cols-4 gap-8 scroll-reveal" :class="{ 'revealed': isVisible.stats }" data-section="stats">
          <div class="text-center group perspective-card">
            <div class="w-16 h-16 gradient-bg rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform duration-300 pulse-glow card-3d">
              <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z"></path>
              </svg>
            </div>
            <div class="text-3xl font-bold text-white mb-2 text-shadow">241</div>
            <div class="text-gray-300">Projects Completed</div>
          </div>

          <div class="text-center group perspective-card">
            <div class="w-16 h-16 gradient-bg rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform duration-300 pulse-glow card-3d">
              <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"></path>
              </svg>
            </div>
            <div class="text-3xl font-bold text-white mb-2 text-shadow">150+</div>
            <div class="text-gray-300">Happy Clients</div>
          </div>

          <div class="text-center group perspective-card">
            <div class="w-16 h-16 gradient-bg rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform duration-300 pulse-glow card-3d">
              <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"></path>
              </svg>
            </div>
            <div class="text-3xl font-bold text-white mb-2 text-shadow">10+</div>
            <div class="text-gray-300">Years Experience</div>
          </div>

          <div class="text-center group perspective-card">
            <div class="w-16 h-16 gradient-bg rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform duration-300 pulse-glow card-3d">
              <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2-2v2m8 0V6a2 2 0 012 2v6a2 2 0 01-2 2H6a2 2 0 01-2-2V8a2 2 0 012-2V6"></path>
              </svg>
            </div>
            <div class="text-3xl font-bold text-white mb-2 text-shadow">25+</div>
            <div class="text-gray-300">Awards Won</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, onMounted } from 'vue';
import BlurReveal from './ui/blur-reveal/BlurReveal.vue';
const aboutheroImage = ref('/about_hero.png')

export default {
  name: 'AboutSection',
  components: {
    BlurReveal,
  },
  setup() {
    const leftImage = ref('/left-bg.png');
    const isVisible = ref({
      hero: false,
      experience: false,
      content: false,
      stats: false,
    });

    const setupScrollReveal = () => {
      const observer = new IntersectionObserver(
        (entries) => {
          entries.forEach((entry) => {
            if (entry.isIntersecting) {
              const target = entry.target;
              if (target.classList.contains('scroll-reveal')) {
                const section = target.dataset.section;
                if (section) {
                  isVisible.value[section] = true;
                }
              }
            }
          });
        },
        {
          threshold: 0.1,
          rootMargin: '50px',
        }
      );

      const elements = document.querySelectorAll('.scroll-reveal');
      elements.forEach((el) => observer.observe(el));
    };

    onMounted(() => {
      setupScrollReveal();
    });

    return {
      isVisible,
      aboutheroImage
    };
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap');

* {
  font-family: 'Inter', sans-serif;
}

.gradient-text {
  background: linear-gradient(135deg, #ec4899 0%, #ef4444 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.gradient-bg {
  background: linear-gradient(135deg, #ec4899 0%, #ef4444 100%);
}

.glass-effect {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.bg-mesh {
  background-image: 
    radial-gradient(circle at 20% 20%, rgba(236, 72, 153, 0.15) 0%, transparent 50%),
    radial-gradient(circle at 80% 80%, rgba(239, 68, 68, 0.15) 0%, transparent 50%),
    radial-gradient(circle at 40% 40%, rgba(168, 85, 247, 0.1) 0%, transparent 50%),
    radial-gradient(circle at 60% 20%, rgba(59, 130, 246, 0.1) 0%, transparent 50%);
  background-size: 100% 100%, 80% 80%, 60% 60%, 40% 40%;
  animation: mesh-move 20s ease-in-out infinite;
}

@keyframes mesh-move {
  0%, 100% { background-position: 0% 0%, 100% 100%, 0% 100%, 100% 0%; }
  25% { background-position: 100% 0%, 0% 100%, 100% 100%, 0% 0%; }
  50% { background-position: 100% 100%, 0% 0%, 100% 0%, 0% 100%; }
  75% { background-position: 0% 100%, 100% 0%, 0% 0%, 100% 100%; }
}

.floating-element {
  animation: float 6s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  33% { transform: translateY(-20px) rotate(1deg); }
  66% { transform: translateY(-10px) rotate(-1deg); }
}

.pulse-glow {
  animation: pulse-glow 3s ease-in-out infinite;
}

@keyframes pulse-glow {
  0%, 100% { box-shadow: 0 0 30px rgba(236, 72, 153, 0.3); }
  50% { box-shadow: 0 0 60px rgba(236, 72, 153, 0.6); }
}

.hover-lift {
  transition: all 0.3s ease;
}

.hover-lift:hover {
  transform: translateY(-5px);
}

.perspective-card {
  perspective: 1000px;
}

.card-3d {
  transform-style: preserve-3d;
  transition: transform 0.6s;
}

.card-3d:hover {
  transform: rotateY(5deg) rotateX(5deg);
}

.text-shadow {
  text-shadow: 0 0 20px rgba(236, 72, 153, 0.5);
}

.bg-pattern {
  background-image: 
    linear-gradient(45deg, transparent 40%, rgba(255, 255, 255, 0.01) 50%, transparent 60%),
    linear-gradient(-45deg, transparent 40%, rgba(255,255,255,0.01) 50%, transparent 60%);
  background-size: 20px 20px;
  animation: pattern-move 10s linear infinite;
}

@keyframes pattern-move {
  0% { background-position: 0 0, 0 0; }
  100% { background-position: 20px 20px, -20px -20px; }
}

.neon-border {
  position: relative;
  overflow: hidden;
}

.neon-border::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  padding: 2px;
  background: linear-gradient(45deg, #ec4899, #ef4444, #8b5cf6, #06b6d4, #ec4899);
  background-size: 200% 200%;
  animation: neon-border-move 3s linear infinite;
  border-radius: inherit;
  mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  mask-composite: exclude;
}

@keyframes neon-border-move {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.scroll-reveal {
  opacity: 0;
  transform: translateY(50px);
  transition: all 0.8s ease-out;
}

.scroll-reveal.revealed {
  opacity: 1;
  transform: translateY(0);
}
</style>