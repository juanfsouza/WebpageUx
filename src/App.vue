<template>
  <div id="app">
    <PortfolioHero />
    <AboutSection />
    <ProjectsSection />
    <FooterSection />
    <ScrollToTop />
  </div>
</template>

<script setup lang="ts">
import PortfolioHero from '@/components/PortfolioHero.vue'
import AboutSection from '@/components/AboutSection.vue'
import ProjectsSection from '@/components/ProjectsSection.vue'
import FooterSection from '@/components/FooterSection.vue'
import ScrollToTop from '@/components/ScrollToTop.vue'
</script>

<style>
#app {
  min-height: 100vh;
  overflow-x: hidden;
}
</style>