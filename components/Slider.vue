<template>
  <div v-swiper="swiperOption">
    <div class="swiper-wrapper">
      <div class="swiper-slide">
        <img src="@/assets/img/slider-1.jpg" alt="" />
      </div>
      <div class="swiper-slide">
        <img src="@/assets/img/slider-2.jpg" alt="" />
      </div>
      <div class="swiper-slide">
        <img src="@/assets/img/slider-2.jpg" alt="" />
      </div>
      <div class="swiper-slide">
        <img src="@/assets/img/slider-2.jpg" alt="" />
      </div>
    </div>
    <div class="swiper-pagination swiper-pagination-bullets"></div>
  </div>
</template>

<script>
import { directive } from "vue-awesome-swiper";

export default {
  data() {
    return {
      swiperOption: {
        slidesPerView: "auto",

        spaceBetween: 30,
        pagination: {
          el: ".swiper-pagination",
          dynamicBullets: true,
          clickable: true,
        },
      },
    };
  },
  directives: {
    swiper: directive,
  },
};
</script>

<style lang="scss" scoped>
.swiper-container {
  height: 400px;
  max-width: 1200px;
  .swiper-slide {
    width: 80%;
    // text-align: center;
    font-size: 38px;
    font-weight: 700;
    background-color: #eee;
    flex-shrink: 1;
    // display: flex;
    // justify-content: center;
    // align-items: center;
    .swiper-slide:nth-child(2n) {
      width: 40%;
    }
    .swiper-slide:nth-child(3n) {
      width: 20%;
    }
    img {
      display: block;
      object-fit: cover;
    }
  }
  .swiper-pagination {
    position: absolute;
    text-align: center;
    transition: opacity 0.3s;
    transform: translateZ(0);
    z-index: 10;
    > .swiper-pagination-bullet {
      background-color: red;
    }
  }
}
</style>