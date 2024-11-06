<template>
  <div class="my-32">
    <h1 class="text-center font-semibold text-5xl my-12">Look what our users say about our product</h1>
    <p class="text-center text-gray-500 max-w-3xl mx-auto my-5">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Adipisci praesentium voluptate natus sed dolor doloribus, beatae perspiciatis modi. Repudiandae excepturi nam dolorum dolorem maxime cumque minima, consequuntur voluptas facere ad.</p>
      <Swiper
          :modules="modules"
          :slides-per-view="1"
          :space-between="10"
          :auto-height="true"
          :Autoplay="true"
          :breakpoints="{
            640: { slidesPerView: 1, spaceBetween: 10 },
            768: { slidesPerView: 2, spaceBetween: 10 },
            1024: { slidesPerView: 3, spaceBetween: 10 }
          }"
          :loop="true"
      >
          <SwiperSlide v-for="card in feedbackCards" :key="card.id" class="flex justify-center items-center mx-20">
              <FeedbackCard
                  :name="card.user"
                  :message="card.cardDesc"
                  :rating="card.rating"
                  :image="card.image"
              />
          </SwiperSlide>
      </Swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/scrollbar';
import { Navigation, Pagination,  Autoplay, Scrollbar, A11y } from "swiper/modules";

import FeedbackCard from './feedbackCard.vue';

export default {
  components: {
      FeedbackCard,
      Swiper, SwiperSlide

  },
  setup() {
      // Feedback data for the cards
      const feedbackCards = [
          {
              id: 1,
              user: "John Doe",
              cardDesc: "Great product! Really satisfied with the quality and performance.",
              rating: 5,
              image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR-WZCN_jqspLOle2tIsl_fgAfDOv_vySTHgO6T4lR3u_z0IqWDKsRYhR_iIoflxjQ80nk&usqp=CAU'
          },
          {
              id: 2,
              user: "Jane Smith",
              cardDesc: "It's okay, could be better. The features are great but it lacks speed.",
              rating: 3,
              image: 'https://images.unsplash.com/photo-1500648767791-00dcc994a43e?fm=jpg&q=60&w=3000&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8cG9ydHJhaXR8ZW58MHx8MHx8fDA%3D'
          },
          {
              id: 3,
              user: "Alice Johnson",
              cardDesc: "Amazing customer service. Loved the attention to detail.",
              rating: 4,
              image: 'https://thumbs.dreamstime.com/b/middle-aged-man-smiling-29650221.jpg'
          },
          {
              id: 4,
              user: "Michael Brown",
              cardDesc: "Not worth the price, unfortunately. Expected more functionality.",
              rating: 3,
              image : 'https://c.pxhere.com/photos/08/46/photo-6473.jpg!s2'
          }
      ];

      return {
          modules: [Navigation, Pagination, Scrollbar, Autoplay, A11y],
          feedbackCards
      };
  }
}
</script>
