<template>
  <div>
    <Home-input></Home-input>
    <div style="padding: 5% 0;background:#59bafe">
      <Home-swiper :swiperList="swiperList"></Home-swiper>
    </div>
    <div style="margin-top:3%;">
      <Home-icon :iconlist="iconlist"></Home-icon>
    </div>
    <div style="display:flex;justify-content:space-between;width:90%;margin:5% auto;">
      <Home-mode1
        v-for="(item,index) in hotDatas"
        :key="index"
        :title="item.title"
        :des="item.des"
        :icon="item.icon"
      ></Home-mode1>
    </div>
    <Enter-supper></Enter-supper>
    <div class="foot"></div>
    <Home-bottom :page="0"></Home-bottom>
  </div>
</template>
<script>
import HomeInput from "./Homes/homeInput";
import HomeSwiper from "./Homes/homeSwiper";
import HomeIcon from "./Homes/homeIcon";
import HomeBottom from "./Common/CommonBotton";
import HomeMode1 from "./Common/mode1";
import EnterSupper from "./Common/enterSupper";
import axios from "axios";

export default {
  components: {
    HomeSwiper,
    HomeInput,
    HomeIcon,
    HomeMode1,
    HomeBottom,
    EnterSupper
  },
  name: "Home",
  data() {
    return {
      swiperList: [],
      iconlist: [],
      hotDatas: [
        {
          title: "电影",
          des: "立减8元",
          icon: "static/mock/img/movie.png"
        },
        {
          title: "晚餐",
          des: "专享特价",
          icon: "static/mock/img/hold.png"
        },
        {
          title: "宵夜",
          des: "立减15元",
          icon: "static/mock/img/rain.png"
        }
      ]
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
      res = res.data;
      if (res.ret && res.data) {
        this.swiperList = res.data.swiperList;
        this.iconlist = res.data.iconlist;
        this.hotArr = res.data.hotArr;
        this.weekendArr = res.data.weekendArr;
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
.foot {
  margin-bottom: 22%;
}
</style>

