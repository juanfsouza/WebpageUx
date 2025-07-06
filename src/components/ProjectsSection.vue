<template>
  <div class="min-h-screen bg-gradient-to-br from-gray-900 via-black to-purple-900 text-white relative overflow-hidden">
    <div class="absolute top-1/5 right-2/3 w-[1000px] h-[300px] bg-black/80 rounded-full blur-3xl z-10"></div>
    <div class="absolute top-1/5 left-2/3 w-[1000px] h-[300px] bg-black/80 rounded-full blur-3xl z-10"></div>
    <div class="absolute inset-0 bg-black"></div>
    
    <!-- Animated Background -->
    <div class="absolute inset-0 bg-mesh bg-pattern opacity-80"></div>
    
    <!-- Floating Background Elements -->
    <div class="absolute top-20 left-10 w-96 h-96 bg-gradient-to-br from-pink-500/20 to-purple-600/10 rounded-full blur-3xl floating-element"></div>
    <div class="absolute bottom-20 right-10 w-80 h-80 bg-gradient-to-br from-red-500/20 to-pink-600/10 rounded-full blur-3xl floating-element" style="animation-delay: -2s;"></div>
    <div class="absolute top-1/2 left-1/4 w-64 h-64 bg-gradient-to-br from-blue-500/10 to-purple-600/10 rounded-full blur-3xl floating-element" style="animation-delay: -4s;"></div>
    
    <!-- Main Content -->
    <div class="relative z-0 py-20 px-6">
      <div class="max-w-7xl mx-auto">
        <!-- Header Section -->
        <div class="text-center mb-16">
          <BlurReveal :delay="0.5" :duration="2.0" :blur="'20px'" :yOffset="50">
            <div class="text-pink-500 font-semibold text-sm tracking-wider uppercase mb-4">
              MY WORK
            </div>
            <h2 class="text-4xl lg:text-6xl font-bold text-white mb-6 leading-tight text-shadow">
              Featured <span class="gradient-text">Projects</span>
            </h2>
            <p class="text-gray-300 text-lg max-w-2xl mx-auto">
              Explore my latest work and creative solutions. Each project showcases my approach to design and development.
            </p>
          </BlurReveal>
        </div>

        <!-- Projects Grid -->
        <div class="grid lg:grid-cols-3 md:grid-cols-2 gap-8 mb-20">
          <div 
            v-for="project in projects" 
            :key="project.id"
            class="glass-effect rounded-2xl overflow-hidden hover-lift card-3d transition-all duration-300 group cursor-pointer scroll-reveal"
            :class="{ 'revealed': isVisible.projects }"
            data-section="projects"
          >
            <!-- Project Image -->
            <div class="relative overflow-hidden h-48 bg-gradient-to-br from-pink-500/20 to-purple-600/20">
              <div class="absolute inset-0 bg-gradient-to-br from-pink-500/10 to-purple-600/10 group-hover:from-pink-500/20 group-hover:to-purple-600/20 transition-all duration-300"></div>
              <div class="absolute inset-0 flex items-center justify-center">
                <div class="w-16 h-16 gradient-bg rounded-full flex items-center justify-center group-hover:scale-110 transition-transform duration-300">
                  <component :is="project.icon" class="w-8 h-8 text-white" />
                </div>
              </div>
              <!-- Project Category Badge -->
              <div class="absolute top-4 left-4">
                <span class="px-3 py-1 bg-black/50 backdrop-blur-sm rounded-full text-xs font-medium text-white">
                  {{ project.category }}
                </span>
              </div>
            </div>

            <!-- Project Info -->
            <div class="p-6">
              <h3 class="text-xl font-bold text-white mb-2 group-hover:text-pink-400 transition-colors duration-300">
                {{ project.title }}
              </h3>
              <p class="text-gray-300 text-sm mb-4 leading-relaxed">
                {{ project.description }}
              </p>
              
              <!-- Technologies Used -->
              <div class="flex flex-wrap gap-2 mb-4">
                <span 
                  v-for="tech in project.technologies" 
                  :key="tech"
                  class="px-2 py-1 bg-white/5 rounded-md text-xs text-gray-300 border border-white/10"
                >
                  {{ tech }}
                </span>
              </div>

              <!-- Project Links -->
              <div class="flex justify-between items-center">
                <div class="flex space-x-3">
                  <button class="flex items-center space-x-2 text-pink-400 hover:text-pink-300 transition-colors duration-300">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"></path>
                    </svg>
                    <span class="text-sm">Live Demo</span>
                  </button>
                  <button class="flex items-center space-x-2 text-gray-400 hover:text-white transition-colors duration-300">
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path>
                    </svg>
                    <span class="text-sm">Code</span>
                  </button>
                </div>
                <div class="text-gray-500 text-sm">
                  {{ project.year }}
                </div>
              </div>
            </div>
          </div>
        </div>

        <img 
          :src="bgrImage" 
          alt="bg-right" 
          class="w-[1000px] h-[1000px] top-2/4 left-2/4 transform absolute md:block hidden sway"
        />

        <!-- Skills Section -->
        <div class="grid lg:grid-cols-2 gap-16 mb-20">
          <!-- Design Skills -->
          <div class="scroll-reveal" :class="{ 'revealed': isVisible.designSkills }" data-section="designSkills">
            <div class="flex items-center space-x-3 mb-8">
              <div class="w-12 h-12 gradient-bg rounded-full flex items-center justify-center">
                <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 21a4 4 0 01-4-4V5a2 2 0 012-2h4a2 2 0 012 2v12a4 4 0 01-4 4zM21 5a2 2 0 00-2-2h-4a2 2 0 00-2 2v6a2 2 0 002 2h4a2 2 0 002-2V5z"></path>
                </svg>
              </div>
              <h3 class="text-2xl font-bold text-white">Design Skill</h3>
            </div>
            
            <div class="space-y-6">
              <div v-for="skill in designSkills" :key="skill.name" class="group">
                <div class="flex justify-between items-center mb-2">
                  <span class="text-white font-medium">{{ skill.name }}</span>
                  <span class="text-pink-400 font-semibold">{{ skill.percentage }}%</span>
                </div>
                <div class="w-full bg-white/10 rounded-full h-2">
                  <div 
                    class="h-2 rounded-full gradient-bg transition-all duration-1000 ease-out"
                    :style="{ width: isVisible.designSkills ? skill.percentage + '%' : '0%' }"
                  ></div>
                </div>
              </div>
            </div>
          </div>

          <!-- Development Skills -->
          <div class="scroll-reveal" :class="{ 'revealed': isVisible.devSkills }" data-section="devSkills">
            <div class="flex items-center space-x-3 mb-8">
              <div class="w-12 h-12 gradient-bg rounded-full flex items-center justify-center">
                <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path>
                </svg>
              </div>
              <h3 class="text-2xl font-bold text-white">Development Skill</h3>
            </div>
            
            <div class="space-y-6">
              <div v-for="skill in developmentSkills" :key="skill.name" class="group">
                <div class="flex justify-between items-center mb-2">
                  <span class="text-white font-medium">{{ skill.name }}</span>
                  <span class="text-pink-400 font-semibold">{{ skill.percentage }}%</span>
                </div>
                <div class="w-full bg-white/10 rounded-full h-2">
                  <div 
                    class="h-2 rounded-full gradient-bg transition-all duration-1000 ease-out"
                    :style="{ width: isVisible.devSkills ? skill.percentage + '%' : '0%' }"
                  ></div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Experience & Education -->
        <div class="grid lg:grid-cols-2 gap-16">
          <!-- Experience -->
          <div class="scroll-reveal" :class="{ 'revealed': isVisible.experience }" data-section="experience">
            <div class="flex items-center space-x-3 mb-8">
              <div class="w-12 h-12 gradient-bg rounded-full flex items-center justify-center">
                <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2-2v2m8 0V6a2 2 0 012 2v6a2 2 0 01-2 2H6a2 2 0 01-2-2V8a2 2 0 012-2V6"></path>
                </svg>
              </div>
              <h3 class="text-2xl font-bold text-white">My Experience</h3>
            </div>
            
            <div class="space-y-6">
              <div v-for="exp in experience" :key="exp.id" class="glass-effect rounded-xl p-6 hover-lift transition-all duration-300">
                <div class="flex items-start space-x-4">
                  <div class="w-3 h-3 gradient-bg rounded-full mt-2 flex-shrink-0"></div>
                  <div class="flex-1">
                    <div class="text-pink-400 text-sm font-medium mb-1">{{ exp.period }}</div>
                    <h4 class="text-white font-bold text-lg mb-1">{{ exp.position }}</h4>
                    <p class="text-gray-400 text-sm">{{ exp.company }}</p>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Education -->
          <div class="scroll-reveal" :class="{ 'revealed': isVisible.education }" data-section="education">
            <div class="flex items-center space-x-3 mb-8">
              <div class="w-12 h-12 gradient-bg rounded-full flex items-center justify-center">
                <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 14l9-5-9-5-9 5 9 5zm0 0l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z"></path>
                </svg>
              </div>
              <h3 class="text-2xl font-bold text-white">My Education</h3>
            </div>
            
            <div class="space-y-6">
              <div v-for="edu in education" :key="edu.id" class="glass-effect rounded-xl p-6 hover-lift transition-all duration-300">
                <div class="flex items-start space-x-4">
                  <div class="w-3 h-3 gradient-bg rounded-full mt-2 flex-shrink-0"></div>
                  <div class="flex-1">
                    <div class="text-pink-400 text-sm font-medium mb-1">{{ edu.period }}</div>
                    <h4 class="text-white font-bold text-lg mb-1">{{ edu.course }}</h4>
                    <p class="text-gray-400 text-sm">{{ edu.institution }}</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, onMounted } from 'vue';
import BlurReveal from './ui/blur-reveal/BlurReveal.vue';
const bgrImage = ref('/bg-r.png')

export default {
  name: 'ProjectsSection',
  components: {
    BlurReveal,
  },
  setup() {
    const isVisible = ref({
      projects: false,
      designSkills: false,
      devSkills: false,
      experience: false,
      education: false,
    });

    // Projects data
    const projects = ref([
      {
        id: 1,
        title: 'E-commerce Platform',
        description: 'A modern e-commerce solution with real-time inventory management and secure payment processing.',
        category: 'Web Development',
        technologies: ['Vue.js', 'Node.js', 'MongoDB', 'Stripe'],
        year: '2024',
        icon: 'ShoppingCart'
      },
      {
        id: 2,
        title: 'Mobile Banking App',
        description: 'Secure mobile banking application with biometric authentication and real-time transactions.',
        category: 'Mobile App',
        technologies: ['React Native', 'Firebase', 'API Integration'],
        year: '2023',
        icon: 'Smartphone'
      },
      {
        id: 3,
        title: 'Brand Identity Design',
        description: 'Complete brand identity design including logo, typography, and brand guidelines.',
        category: 'Design',
        technologies: ['Photoshop', 'Illustrator', 'Figma'],
        year: '2024',
        icon: 'Palette'
      },
      {
        id: 4,
        title: 'SaaS Dashboard',
        description: 'Analytics dashboard for SaaS companies with real-time data visualization and reporting.',
        category: 'Web Development',
        technologies: ['React', 'D3.js', 'Node.js', 'PostgreSQL'],
        year: '2023',
        icon: 'BarChart'
      },
      {
        id: 5,
        title: 'Restaurant Website',
        description: 'Modern restaurant website with online ordering system and reservation management.',
        category: 'Web Development',
        technologies: ['Vue.js', 'Tailwind CSS', 'Laravel', 'MySQL'],
        year: '2024',
        icon: 'Utensils'
      },
      {
        id: 6,
        title: 'Portfolio Website',
        description: 'Creative portfolio website for a photographer with interactive galleries and contact forms.',
        category: 'Web Design',
        technologies: ['HTML5', 'CSS3', 'JavaScript', 'GSAP'],
        year: '2023',
        icon: 'Camera'
      }
    ]);

    // Skills data
    const designSkills = ref([
      { name: 'Photoshop', percentage: 100 },
      { name: 'Figma', percentage: 95 },
      { name: 'Adobe XD', percentage: 60 },
      { name: 'Adobe Illustrator', percentage: 70 }
    ]);

    const developmentSkills = ref([
      { name: 'HTML', percentage: 100 },
      { name: 'CSS', percentage: 95 },
      { name: 'JavaScript', percentage: 60 },
      { name: 'WordPress', percentage: 70 }
    ]);

    // Experience data
    const experience = ref([
      {
        id: 1,
        period: '2022 - Present',
        position: 'Senior Developer',
        company: 'CodeGenius (USA)'
      },
      {
        id: 2,
        period: '2022 - 2022',
        position: 'Web Developer',
        company: 'Modern Tomoli'
      },
      {
        id: 3,
        period: '2020 - 2022',
        position: 'UI Designer',
        company: 'Tech Design Company'
      },
      {
        id: 4,
        period: '2016 - 2019',
        position: 'Intern UI/UX Designer',
        company: 'USA Web Company'
      }
    ]);

    // Education data
    const education = ref([
      {
        id: 1,
        period: '2020 - 2023',
        course: 'Programming Course',
        institution: 'Harvard University'
      },
      {
        id: 2,
        period: '2016 - 2020',
        course: 'Graphic Design Course',
        institution: 'University of Denmark'
      },
      {
        id: 3,
        period: '2012 - 2015',
        course: 'Web Design Course',
        institution: 'University of California'
      },
      {
        id: 4,
        period: '2010 - 2011',
        course: 'Design & Technology',
        institution: 'Parsons, The New School'
      }
    ]);

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
      projects,
      designSkills,
      developmentSkills,
      experience,
      education,
      bgrImage
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

.hover-lift {
  transition: all 0.3s ease;
}

.hover-lift:hover {
  transform: translateY(-5px);
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

.scroll-reveal {
  opacity: 0;
  transform: translateY(50px);
  transition: all 0.8s ease-out;
}

.scroll-reveal.revealed {
  opacity: 1;
  transform: translateY(0);
}

.ShoppingCart, .Smartphone, .Palette, .BarChart, .Utensils, .Camera {
  width: 2rem;
  height: 2rem;
  stroke: currentColor;
  fill: none;
  stroke-width: 2;
  stroke-linecap: round;
  stroke-linejoin: round;
}

.sway {
  animation: sway 3s ease-in-out infinite;
  animation-delay: 1.5s;
}

@keyframes sway {
  0%, 100% { transform: translateX(0); }
  50% { transform: translateX(-20px); }
}

</style>