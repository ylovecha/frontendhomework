<template>
  <div class="swiper-container">
    <div class="swiper-wrapper">
      <div class="swiper-slide">Slide 1</div>
      <div class="swiper-slide">Slide 2</div>
      <div class="swiper-slide">Slide 3</div>
    </div>
    <div class="swiper-pagination"></div>
  </div>
</template>
<script>
import Swiper from "swiper";
import "swiper/css/swiper.css";
export default {
  mounted() {
    new Swiper(".swiper-container", {
      pagination: { el: ".swiper-pagination" },
    });
  },
};
</script>
<style scoped>
.swiper-container {
  width: 100%;
  height: 300px;
}
.swiper-slide {
  text-align: center;
  font-size: 30px;
  background: #fff;
}
</style>
