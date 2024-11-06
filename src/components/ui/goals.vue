<template>
    <section class="bg-primary py-12">
      <h1 class="text-center text-white font-bold text-6xl pb-20">Our Goals</h1>
      
      <div class="container mx-auto px-4 max-w-7xl">
        <!-- Timeline Row -->
        <div class="relative flex justify-between space-x-16">
          <!-- Timeline Line -->
          
          <!-- Goal 1 -->
          <div class="flex items-center relative z-10 w-1/3">
            <div class="bg-white p-6 rounded-lg shadow-lg w-full">
              <h3 class="text-xl font-semibold text-gray-700 mb-4 flex items-center">
                <Activity class="mr-3 text-primary w-8 h-8" /> 
                Achieve Fitness Goals
              </h3>
              <p class="text-gray-600">
                Our primary goal is to help you <span class="text-primary">reach your fitness goals</span> with the best tools and tracking features. Whether you’re looking to lose weight, gain muscle, or just stay healthy, we’re here to guide you every step of the way.
              </p>
            </div>
          </div>
  
          <!-- Goal 2 -->
          <div class="flex items-center relative z-10 w-1/3">
            <div class="bg-white p-6 rounded-lg shadow-lg w-full py-12">
              <h3 class="text-xl font-semibold text-gray-700 mb-4 flex items-center">
                <Watch class="mr-3 text-primary w-8 h-8" /> 
                Time Management
              </h3>
              <p class="text-gray-600">
                With <span class="text-primary">smart scheduling</span>, we help you optimize your workout and rest periods. Achieve more in less time by balancing productivity and health, with reminders to keep you on track.
              </p>
            </div>
          </div>
  
          <!-- Goal 3 -->
          <div class="flex items-center relative z-10 w-1/3">
            <div class="bg-white p-6 rounded-lg shadow-lg w-full">
              <h3 class="text-xl font-semibold text-gray-700 mb-4 flex items-center">
                <Heart class="mr-3 text-primary w-8 h-8" />
                Monitor Your Health
              </h3>
              <p class="text-gray-600">
                Keeping an eye on your <span class="text-primary">heart rate</span>, sleep patterns, and other vital signs helps ensure that you're maintaining optimal health. Our app will help you monitor these key metrics to stay on top of your wellness.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  import { Heart } from 'lucide-vue-next';
  import { Activity } from 'lucide-vue-next';
  import { Watch } from 'lucide-vue-next';
  
  export default {
    name: 'Goals',
    components: {
      Heart,
      Activity,
      Watch
    }
  }
  </script>
  
  <style scoped>
  /* Custom styles */
  .container {
    position: relative;
  }
  </style>
  