<template >
  <div class="px-20">
    <div class="flex justify-between items-center px-6 py-4">
    <div class="flex items-center gap-2">
      <img src="../assets/Screenshot_2024-11-06_095046-removebg-preview.png" class="h-30 w-16">
      <h1 class="text-4xl font-extrabold text-[#56A2A6] uppercase">Rakib</h1>
    </div>

    <div class="hidden md:flex justify-center items-center space-x-8">
      <router-link to="/" class="uppercase text-black hover:text-primary font-sans font-bold">Home</router-link>
      <router-link to="/buy" class="uppercase text-black hover:text-primary font-sans font-bold">Goals</router-link>
      <router-link to="/sell" class="uppercase text-black hover:text-primary font-sans font-bold">Our Product</router-link>
      <router-link to="/rent" class="uppercase text-black hover:text-primary font-sans font-bold">FAQ</router-link>
      <router-link to="/rent" class="uppercase text-black hover:text-primary font-sans font-bold">Help</router-link>
    </div>

    <div class="md:hidden flex items-center" @click="toggleMenu">
      <svg xmlns="" fill="none" viewBox="0 0 24 24" stroke="currentColor" class="h-6 w-6 text-black">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
      </svg>
    </div>
  </div>

  <div v-if="isMenuOpen" class="md:hidden absolute top-16 left-0 w-full bg-white shadow-lg py-4 px-6 space-y-4">
    <router-link to="/" class="uppercase text-black hover:text-primary font-sans font-bold block">Home</router-link>
    <router-link to="/buy" class="uppercase text-black hover:text-primary font-sans font-bold block">Goals</router-link>
    <router-link to="/sell" class="uppercase text-black hover:text-primary font-sans font-bold block">Our Product</router-link>
    <router-link to="/rent" class="uppercase text-black hover:text-primary font-sans font-bold block">FAQ</router-link>
    <router-link to="/rent" class="uppercase text-black hover:text-primary font-sans font-bold block">Help</router-link>
  </div>
  </div>
  
</template>

<script>
import { User } from 'lucide-vue-next';
import { ChevronDown } from 'lucide-vue-next';

export default {
  components: {
    ChevronDown,
    User,
  },
  data() {
    return {
      isMenuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
  },
};
</script>

