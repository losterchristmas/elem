<template>
  <div class="bottom">
    <div class="bottom-list" v-for="(item,index) in iconList" :key="index" :style='index==page?"color:#0c97f4":""'>
      <i :class="item.icon"></i>
      <p>{{item.text}}</p>
    </div>
  </div>
</template>
<script>
export default {
  props:{
    page:Number
  },
  data() {
    return {
      iconList: [
        {
          icon: "el-icon-eleme icon-font-size",
          text: "外卖",
          status:false
        },
        {
          icon: "el-icon-s-shop icon-font-size",
          text: "超市",
          status:false
        },
        {
          icon: "el-icon-tickets icon-font-size",
          text: "订单",
          status:false
        },
        {
          icon: "el-icon-s-custom icon-font-size",
          text: "我的",
          status:false
        }
      ]
    };
  },
};
</script>
<style lang="stylus" scoped>
.bottom {
  width: 100%;
  position: fixed;
  bottom: 0;
  border-top: 1px solid #c6c6c6;
  display: flex;

  .bottom-list {
    width: 25%;
    text-align: center;
      color: #818181;

    .icon-font-size {
      font-size: 1.8rem;
      padding: 7% 0;
    }

    p {
      font-size: 1rem;
      padding-bottom: 7%;
    }
  }
}
</style>
