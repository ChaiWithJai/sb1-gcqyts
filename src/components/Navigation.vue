<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps<{
  activeSection: string;
}>();

const navItems = ['Home', 'About', 'Projects', 'Contact'];

const scrollToSection = (sectionId: string) => {
  const element = document.getElementById(sectionId);
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' });
  }
};
</script>

<template>
  <nav class="fixed top-0 left-0 w-full bg-[#3B1E54] bg-opacity-90 shadow-sm z-50 backdrop-blur-sm">
    <div class="container mx-auto px-6 py-4 flex justify-between items-center">
      <button @click="scrollToSection('home')" class="text-xl font-bold text-[#D4BEE4]">
        Yash Pise
      </button>
      <div class="flex space-x-8">
        <button
          v-for="item in navItems"
          :key="item"
          @click="scrollToSection(item.toLowerCase())"
          :class="[
            'text-sm hover:text-[#D4BEE4] transition-colors',
            activeSection === item.toLowerCase() ? 'text-[#D4BEE4] font-semibold' : 'text-[#9B7EBD]'
          ]"
        >
          {{ item }}
        </button>
      </div>
    </div>
  </nav>
</template>