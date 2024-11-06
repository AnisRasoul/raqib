<template>
  <section class="py-20 bg-gray-50 relative">
    <!-- Background Image -->
    <div class="absolute bottom-0 left-0 w-full h-full bg-[url('../../assets/Background.png')] bg-cover bg-no-repeat bg-bottom opacity-20"></div>

    <!-- Section Title and Subtitle -->
    <div class="text-center mb-12">
      <h2 class="text-3xl font-bold text-gray-800">Frequently Asked Questions</h2>
      <p class="text-xl text-gray-600 mt-2 max-w-3xl mx-auto">
        Find answers to the most common questions about our medical watch app and how it can help you monitor your health.
      </p>
    </div>

    <!-- Accordion Component -->
    <div class="max-w-4xl mx-auto">
      <Accordion type="single" class="grid grid-cols-1 gap-4">
        <AccordionItem
          v-for="item in accordionItems"
          :key="item.value"
          :value="item.value"
          class="bg-white text-black border border-[#033C71] rounded-lg shadow-md"
        >
          <!-- Accordion Trigger (Title) -->
          <AccordionTrigger class="px-6 py-4 text-lg font-semibold text-[#033C71] hover:text-[#012F4D] transition duration-200">
            {{ item.title }}
          </AccordionTrigger>
          <!-- Accordion Content -->
          <AccordionContent class="px-6 py-4 text-gray-700">
            {{ item.content }}
          </AccordionContent>
        </AccordionItem>
      </Accordion>
    </div>
  </section>
</template>

<script>
import Accordion from './accordion/Accordion.vue';
import AccordionContent from './accordion/AccordionContent.vue';
import AccordionItem from './accordion/AccordionItem.vue';
import AccordionTrigger from './accordion/AccordionTrigger.vue';

export default {
  components: {
    Accordion,
    AccordionContent,
    AccordionItem,
    AccordionTrigger,
  },
  data() {
    return {
      accordionItems: [
        {
          value: 'item-1',
          title: 'What features does the medical watch app offer?',
          content: 'Our medical watch app offers real-time health tracking, heart rate monitoring, blood pressure measurement, sleep analysis, step tracking, and much more. It helps you stay on top of your health with detailed insights and daily reports.',
        },
        {
          value: 'item-2',
          title: 'How do I sync the medical watch with the app?',
          content: 'To sync the medical watch with the app, simply download and install the app on your smartphone. Follow the pairing instructions in the app to connect your watch via Bluetooth. Once connected, the app will automatically sync your health data.',
        },
        {
          value: 'item-3',
          title: 'Does the app track my heart rate and sleep patterns?',
          content: 'Yes! The app continuously monitors your heart rate, tracking any irregularities or signs of stress. It also provides detailed insights into your sleep patterns, including deep sleep, light sleep, and sleep efficiency, so you can improve your sleep quality.',
        },
        {
          value: 'item-4',
          title: 'Can the app track my daily activity levels?',
          content: 'Absolutely. The app tracks your daily activity levels, including steps, calories burned, and distance traveled. It provides personalized recommendations to help you stay active and meet your fitness goals.',
        },
        {
          value: 'item-5',
          title: 'Is the app compatible with other health devices?',
          content: 'Yes, our app is designed to work seamlessly with a variety of health devices, including smart scales, blood glucose monitors, and fitness trackers. You can sync your data across devices to get a complete view of your health.',
        },
        {
          value: 'item-6',
          title: 'Is my health data secure in the app?',
          content: 'Your privacy and data security are our top priorities. We use end-to-end encryption to protect your sensitive health data, ensuring that it remains private and secure. You can also control what data you share with healthcare professionals.',
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Custom styling for the background image */
section {
  position: relative;
}

section .absolute {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  top: auto;
  z-index: -1;
  opacity: 0.2; /* Adjust the opacity as needed */
}
</style>
