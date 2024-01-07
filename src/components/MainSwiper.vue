<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
// import { Pagination } from 'swiper'
import 'swiper/css'
import 'swiper/css/pagination'
import { ref } from 'vue';

const swiperBase = ref([
  {
    img: '../assest/img/slider/slide1.png',
    id: 1
  },
  {
    img: '../assest/img/slider/slide1.png',
    id: 2
  },
  {
    img: '../assest/img/slider/slide1.png',
    id: 3
  },
  {
    img: '../assest/img/slider/slide1.png',
    id: 4
  },
])

</script>

<template>
  <Swiper :space-between="20" :loop="true" :pagination="true" :autoplay="{
    delay: 3000,
    disableOnInteraction: false,
    pauseOnMouseEnter: true
  }">
    <Swiper-slide v-for="swiper in swiperBase" :key="swiper.id">
      <div>
        <img :src="swiper.img" :alt="swiper.id">
      </div>
    </Swiper-slide>
  </Swiper>
</template>

<style lang="scss" scoped>
.swiper {
  width: 917px;
  height: 450px;
  background-color: antiquewhite;
}
</style>