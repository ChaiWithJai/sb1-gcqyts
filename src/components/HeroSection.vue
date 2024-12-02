<script setup lang="ts">
import { Github, Linkedin, Mail } from 'lucide-vue-next';
import { ref, onMounted } from 'vue';

const isVisible = ref(false);

onMounted(() => {
  isVisible.value = true;
});
</script>

<template>
  <section
    id="home"
    class="min-h-screen flex items-center justify-center bg-gradient-to-br from-[#3B1E54] to-[#2A1540] text-[#EEEEEE] overflow-hidden"
  >
    <div
      class="container mx-auto px-6 text-center relative"
      :class="{ 'opacity-0': !isVisible, 'fade-up': isVisible }"
    >
      <div
        class="absolute top-0 left-1/2 -translate-x-1/2 w-[600px] h-[600px] bg-[#9B7EBD] rounded-full opacity-10 blur-[120px]"
      ></div>

      <h1 class="text-6xl md:text-8xl font-bold mb-6 gradient-text relative">
        Yash Pise
      </h1>

      <h2
        class="text-xl md:text-3xl mb-12 text-[#9B7EBD] font-light tracking-wide"
      >
        AI & Data Science Innovator
      </h2>

      <div class="flex justify-center space-x-6 mb-16">
        <a
          href="https://github.com/yp0505"
          target="_blank"
          rel="noopener noreferrer"
          class="text-[#9B7EBD] hover:text-[#D4BEE4] transition-colors"
        >
          <Github class="h-7 w-7" />
        </a>
        <a
          href="https://www.linkedin.com/in/yash-pise0505/"
          target="_blank"
          rel="noopener noreferrer"
          class="text-[#9B7EBD] hover:text-[#D4BEE4] transition-colors"
        >
          <Linkedin class="h-7 w-7" />
        </a>
        <a
          href="mailto:yashpise98@gmail.com"
          class="text-[#9B7EBD] hover:text-[#D4BEE4] transition-colors"
        >
          <Mail class="h-7 w-7" />
        </a>
      </div>

      <div class="absolute left-1/2 -translate-x-1/2 bottom-2 animate-bounce">
        <div class="w-6 h-10 border-2 border-[#9B7EBD] rounded-full relative">
          *
          <div
            class="w-1 h-2 bg-[#9B7EBD] absolute top-8 left-1/2 -translate-x-1/2 rounded-full"
          ></div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.fade-up {
  opacity: 1;
  transition: opacity 1s ease-out,
    transform 1s cubic-bezier(0.34, 1.56, 0.64, 1);
}
</style>
