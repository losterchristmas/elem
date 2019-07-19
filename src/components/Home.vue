<template>
  <div>
    <Home-swiper :swiperList="swiperList"></Home-swiper>
  </div>
</template>
<script>
import HomeSwiper from "./Homes/homeSwiper";

export default {
  components: {
    HomeSwiper
  },
  name: "Home",
  data() {
    return {
      swiperList: [{
          id: "01",
          src: "http://img5.imgtn.bdimg.com/it/u=3987907653,720009510&fm=26&gp=0.jpg"
        },
        {
          id: "02",
          src: "http://pic33.nipic.com/20131007/13639685_123501617185_2.jpg"
        },
        {
          id: "03",
          src:
            "http://img5.imgtn.bdimg.com/it/u=8685675,2171717858&fm=26&gp=0.jpg"
        }]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped></style>

