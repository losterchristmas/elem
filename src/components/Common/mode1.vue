<template>
  <div class="content">
    <p class="title">{{title}}</p>
    <i :class="icon" style="float: right;color: #ff3b42;"></i>
    <p class="des">{{des}}</p>
  </div>
</template>
<script>
export default {
  props: {
    title: String,
    des: String,
    icon: String
  },
  mounted() {
  }
};
</script>
<style lang="stylus" scoped>
.content {
  width: 30.33%;
  border-radius: 10px;
  background: #fcf7f1;
  padding: 3%;

  .title {
    font-size: 1.2rem;
    font-weight: bold;
    margin-bottom: 8%;
  }

  des {
    font-size: 0.9rem;
    color: #81807c;
    line-height: 1rem;
  }

  .icon-style {
    float: right;
    color: #ff3b42;
  }
}
</style>
