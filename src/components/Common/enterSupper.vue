<template>
  <div class="supperContent"> 
    <img src="@/assets/img/map.png" alt="">
    <p class="title">加入超级会员·<span class="des">每月领20元红包</span></p>
    <button>立即开通<i class="el-icon-arrow-right"></i></button>
  </div>
</template>
<script>
export default {
  
}
</script>
<style lang="stylus" scoped>
.supperContent
  display flex;
  justify-content space-between
  width 90%
  margin 5% auto
  background #fbdfaf
  border-radius 10px
  padding 3%
  line-height 2rem
  img
    width 1.6rem
    height 1.6rem
  .title
    color #5e501f
    font-size 1rem
    font-weight bold
  .des
    color #5e501f
    font-size .8rem
  button 
    background #fbdfaf
    border 0 
    outline: none;
    outline-color: rgba(255, 255, 255, 0);
    color #5e501f
    font-size .9rem
    width 30%
    text-align end
    padding 0
</style>
