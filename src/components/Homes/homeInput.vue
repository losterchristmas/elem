<template>
  <div class="header">
    <div class="addr">
      <i class="el-icon-location setIcon"></i>颐和中心
      <i class="el-icon-arrow-down"></i>
      <div class="header-right">
        <i class="el-icon-full-screen"></i>
      </div>
    </div>
    <div class="inputFloat">
      <i class="el-icon-search setIcon weightColor"></i>星巴克免运费
    </div>
    <input type="text" value />
  </div>
</template>
<script>
export default {
  props: {},
  data() {
    return {};
  }
};
</script>
<style lang="stylus" scoped>
.header {
  background: linear-gradient(#3899ff, #59bafe);

  .addr {
    width: 90%;
    margin: 0 auto;
    color: #fff;
    line-height: 2rem;
    padding: 0.5rem 0;

    .setIcon {
      color: #fff;
    }

    .header-right {
      float: right;
    }
  }

  .inputFloat {
    position: absolute;
    text-align: center;
    font-size: .8rem;
    color: #bbbbbb;
    width 100%
    line-height 2.2rem
    .weightColor{
      color #767676;
      padding-right 2%
    }
  }

  input {
    width: 94%;
    margin: 0 auto;
    border-radius: 50px;
    line-height: 2rem;
    border: 0px solid #fff;
    display: block;
    outline: none;
    outline-color: rgba(255, 255, 255, 0);
  }
}
</style>
