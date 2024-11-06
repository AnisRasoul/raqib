<template>
  <div class="flex flex-col md:flex-row justify-center items-center h-screen space-y-10 md:space-y-0">
    <!-- Left Column (Text & Button) -->
    <div class="flex flex-col justify-center items-center text-center md:text-left space-y-6 md:space-y-10 w-full md:w-1/2">
      <h1 class="text-black text-3xl md:text-6xl font-bold text-center">
    Take care of your <span class="text-primary">health</span> with the <span class="text-primary">Rakib</span> app
  </h1>

  <!-- Paragraph -->
  <p class="text-black text-lg md:text-xl max-w-xl text-center">
    Stay on top of your wellness goals with the <span class="text-primary">Rakib</span> app on your <span class="text-primary">smart watch</span>. Track workouts, monitor your heart rate, and get personalized health insights—all in one place.
  </p>

      <button class="text-white flex items-center space-x-4 font-semibold text-lg md:text-2xl bg-primary px-8 py-3 rounded-[25px]">
       <span>Download Rakib</span> <Download/>
      </button>
    </div>
    
    <!-- Right Column (Images) -->
    <div class="relative w-full md:w-1/2 flex justify-center">
      <!-- Blue SVGs (background) -->
      <img 
        src="../../assets/blue.svg" 
        alt="Blue Background 1" 
        class="absolute inset-0 z-0"
      >
      <img 
        src="../../assets/blue.svg" 
        alt="Blue Background 2" 
        class="absolute inset-0 z-0"
      >
      
      <!-- Mockup Image (front) -->
      <img 
        src="../../assets/mockup.png" 
        alt="Mockup" 
        class="relative z-10 h-1/2 w-[80%]"
      >
    </div>
  </div>
</template>

<script>
import { Download } from 'lucide-vue-next';

export default {
  name: "HealthSection",
  components: {
    Download
  }
}
</script>
