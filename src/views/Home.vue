<template>
  <div>
     <navbar/>
      <hero/>
      <goals/>
      <showcase/>
      <Feedback/>
      <faq/>
      <help/>
     
    <Footing/>
  </div>
</template>

<script>
import Footing from '@/components/Footing.vue'
import navbar from '@/components/navbar.vue';
import hero from '@/components/ui/hero.vue';
import goals from '@/components/ui/goals.vue';
import showcase from '@/components/ui/showcase.vue';
import faq from '@/components/ui/faq.vue';
import help from '@/components/ui/help.vue';

import { Search, ChevronLeft, ChevronRight } from 'lucide-vue-next';
import Feedback from '../components/ui/feedback/feedback.vue';



export default {
  components: {
    navbar,
    Footing,
    hero,
    goals,
    showcase,
    faq,
    help,
    Feedback,
    Search,
    ChevronLeft,
    ChevronRight,
  },
  computed: {
  },
  data() {
    return {

    };
  },
 
  methods: {

  }
};
</script>

<style>

</style>
