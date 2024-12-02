<script setup lang="ts">
import { ref, onMounted } from 'vue';
import Navigation from './components/Navigation.vue';
import HeroSection from './components/HeroSection.vue';
import AboutSection from './components/AboutSection.vue';
import ProjectsSection from './components/ProjectsSection.vue';
import ContactSection from './components/ContactSection.vue';
import Footer from './components/Footer.vue';

const activeSection = ref('home');

onMounted(() => {
  const handleScroll = () => {
    const sections = ["home", "about", "projects", "contact"];
    const currentSection = sections.find(section => {
      const element = document.getElementById(section);
      if (element) {
        const rect = element.getBoundingClientRect();
        return rect.top <= 100 && rect.bottom >= 100;
      }
      return false;
    });
    if (currentSection) {
      activeSection.value = currentSection;
    }
  };

  window.addEventListener("scroll", handleScroll);
  return () => window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <div class="bg-[#EEEEEE] text-[#3B1E54]">
    <Navigation :active-section="activeSection" />
    <HeroSection />
    <AboutSection />
    <ProjectsSection />
    <ContactSection />
    <Footer />
  </div>
</template>

<style>
@import './assets/styles/main.css';
</style>