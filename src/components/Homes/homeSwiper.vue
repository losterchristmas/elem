<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="swiperList.length">
      <!-- slides -->
      <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper_img" :src="item.src" alt />
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
import "swiper/dist/css/swiper.css";

import { swiper, swiperSlide } from "vue-awesome-swiper";

export default {
  name: "homeSwiper",
  //   components: {
  //     swiper,
  //     swiperSlide
  //   },
  props: {
    swiperList: Array
  },
  data() {
    return {
      swiperOption: {
        pagination: ".swiper-pagination"
      }
    };
  }
};
</script>
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff !important;
}

.wrapper >>> .swiper-pagination-bullets {
  bottom: 5px;
}

.wrapper >>> .swiper-pagination-bullet {
  width: 14px;
  height: 2px;
  border-radius: 0;
}

.wrapper {
  width: 100%;
  height: 0;
  overflow: hidden;
  padding-bottom: 31.25%;
  background-color: transparent;

  .swiper_img {
    width: 90%;
    margin: 0 auto;
    display: block;
    border-radius: 10px;
    height: 31.25vw;
    background-color: transparent;
  }
}
</style>
