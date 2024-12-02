<script setup lang="ts">
import { ref } from 'vue';

const form = ref({
  name: '',
  email: '',
  message: ''
});

const submitForm = () => {
  console.log('Form submitted:', form.value);
  form.value = { name: '', email: '', message: '' };
};
</script>

<template>
  <section id="contact" class="py-20 bg-[#EEEEEE]">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold text-center mb-12 text-[#3B1E54]">Let's Connect</h2>
      <div class="max-w-md mx-auto">
        <p class="text-center mb-8 text-[#3B1E54]">
          Ready to innovate together? Reach out and let's explore how we can create extraordinary value for your business.
        </p>
        <form class="space-y-4" @submit.prevent="submitForm">
          <input 
            v-model="form.name"
            type="text" 
            placeholder="Your Name" 
            class="w-full p-2 border border-[#9B7EBD] rounded bg-white text-[#3B1E54]"
          />
          <input 
            v-model="form.email"
            type="email" 
            placeholder="Your Email" 
            class="w-full p-2 border border-[#9B7EBD] rounded bg-white text-[#3B1E54]"
          />
          <textarea 
            v-model="form.message"
            placeholder="Your Message" 
            rows="5" 
            class="w-full p-2 border border-[#9B7EBD] rounded bg-white text-[#3B1E54]"
          ></textarea>
          <button 
            type="submit" 
            class="w-full bg-[#3B1E54] text-[#EEEEEE] py-2 px-6 rounded hover:bg-[#9B7EBD] transition-colors"
          >
            Send Message
          </button>
        </form>
      </div>
    </div>
  </section>
</template>