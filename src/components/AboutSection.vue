<script setup lang="ts">
import { PROFILE_IMAGES } from '../config/constants';
</script>

<template>
  <section id="about" class="py-20 bg-[#EEEEEE]">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold text-center mb-12 text-[#3B1E54]">About Me</h2>
      <div class="flex flex-col md:flex-row items-center justify-between">
        <div class="md:w-1/3 mb-8 md:mb-0">
          <div class="relative w-64 h-64 mx-auto">
            <img 
              :src="PROFILE_IMAGES.PROFILE"
              alt="Yash Pise"
              class="rounded-full object-cover shadow-lg w-full h-full"
            />
          </div>
        </div>
        <div class="md:w-2/3 md:pl-12">
          <p class="mb-6 text-[#3B1E54]">
            As a Data Scientist at Johnson & Johnson, I leverage AI and machine learning to revolutionize healthcare and drive business innovation. My work has directly contributed to a 30% improvement in document processing efficiency and achieved 90% accuracy in LLM retrieval patterns.
          </p>
          <p class="mb-6 text-[#3B1E54]">
            With a proven track record of transforming complex data into actionable insights, I've helped Fortune 500 companies optimize their operations and unlock new revenue streams. My expertise bridges the gap between data science and tangible business outcomes.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>