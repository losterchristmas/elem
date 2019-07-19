<template>
  <div>
    <Home-input></Home-input>
    <div style="padding: 5% 0;background:#59bafe">
      <Home-swiper :swiperList="swiperList"></Home-swiper>
    </div>
    <div style="margin-top:3%;">
      <Home-icon :iconlist="iconlist"></Home-icon>
    </div>
    <Home-bottom :page="0"></Home-bottom>
  </div>
</template>
<script>
import HomeInput from "./Homes/homeInput";
import HomeSwiper from "./Homes/homeSwiper";
import HomeIcon from "./Homes/homeIcon";
import HomeBottom from "./Common/CommonBotton";
import axios from "axios";

export default {
  components: {
    HomeSwiper,
    HomeInput,
    HomeIcon,
    HomeBottom
  },
  name: "Home",
  data() {
    return {
      swiperList: [],
      iconlist:[]
    };
  },
  mounted() {
    this.getInfo();
  },
  methods: {
    getInfo() {
      axios
        .get("https://losterchristmas.github.io/travel/static/mock/index.json")
        .then(this.getInfoSucc);
    },
    getInfoSucc(res) {
      console.log(res);
      res = res.data
      if(res.ret&&res.data){
        this.swiperList = res.data.swiperList
        this.iconlist =  res.data.iconlist
        this.hotArr =  res.data.hotArr
        this.weekendArr =  res.data.weekendArr
        
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped></style>

