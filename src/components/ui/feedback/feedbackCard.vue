<template>
    <div class="max-w-sm rounded-lg shadow-lg p-6 bg-white ">
      <!-- User Avatar -->
      <div v-if="image" class="flex items-center mb-4">
        <img :src="image" alt="User Avatar" class="w-12 h-12 rounded-full object-cover mr-4" />
        <div>
          <div class="font-semibold text-2xl text-gray-900 mb-1">{{ name }}</div>
        </div>
      </div>
      <div v-else>
        <div class="font-semibold text-2xl text-gray-900 mb-2">{{ name }}</div>
      </div>
  
      <!-- Feedback Message -->
      <p class="text-gray-600 text-base mb-4 leading-relaxed">{{ message }}</p>
  
      <!-- Rating Section -->
      <div class="flex items-center">
        <!-- Render filled stars -->
        <span v-for="n in rating" :key="'filled-' + n" class="text-yellow-500 text-xl">★</span>
  
        <!-- Render empty stars -->
        <span v-for="n in (5 - rating)" :key="'empty-' + n" class="text-gray-300 text-xl">★</span>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'FeedbackCard',
    props: {
      name: {
        type: String,
        required: true
      },
      message: {
        type: String,
        required: true
      },
      rating: {
        type: Number,
        required: true,
        validator: value => value >= 0 && value <= 5
      },
      image: {
        type: String,
        required: false, // Image is optional
        default: ''
      }
    }
  }
  </script>
  
  <style scoped>
  /* Custom Styling */
  .feedback-card {
    transition: transform 0.2s ease, box-shadow 0.3s ease;
  }
  
  .feedback-card:hover {
    transform: translateY(-5px); /* Lift effect */
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1); /* Slight shadow on hover */
  }
  
  .text-xl {
    font-size: 1.25rem;
  }
  
  .text-2xl {
    font-size: 1.5rem;
  }
  
  .w-12 {
    width: 3rem;
  }
  
  .h-12 {
    height: 3rem;
  }
  
  .rounded-full {
    border-radius: 9999px;
  }
  
  .object-cover {
    object-fit: cover;
  }
  </style>
  