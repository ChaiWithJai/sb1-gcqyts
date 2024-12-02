<script setup lang="ts">
import { PROJECTS } from '../config/constants';

interface Project {
  title: string;
  description: string;
  image: string;
}
</script>

<template>
  <section id="projects" class="py-20 bg-[#9B7EBD]">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold text-center mb-12 text-[#EEEEEE]">Key Projects</h2>
      <div class="grid md:grid-cols-3 gap-8">
        <div v-for="(project, index) in PROJECTS" :key="index" class="bg-[#D4BEE4] rounded-lg overflow-hidden shadow-md">
          <div class="relative w-full h-48">
            <img 
              :src="project.image"
              :alt="project.title"
              class="object-cover w-full h-full"
            />
          </div>
          <div class="p-6">
            <h3 class="text-xl font-semibold mb-2 text-[#3B1E54]">{{ project.title }}</h3>
            <p class="text-[#3B1E54]">{{ project.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>