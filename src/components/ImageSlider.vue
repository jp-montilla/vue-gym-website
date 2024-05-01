<template>
  <Carousel class="carousel-container">
    <Slide v-for="slide in 10" :key="slide">
      <div class="carousel__item"><img src="https://placehold.co/1200x800" alt=""></div>
    </Slide>

    <template #addons>
      <Navigation />
      <!-- <Pagination /> -->
    </template>
  </Carousel>
</template>

<script setup>
import { defineComponent } from 'vue'
import { Carousel, Navigation, Pagination, Slide } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css'


</script>


<style scoped>
.carousel-container {
    width: 50%;
}
.carousel__item {
  min-height: 200px;
  width: 50%;
  color: var(--vc-clr-white);
  font-size: 20px;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel__slide {
  padding: 10px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid white;
}

</style>

