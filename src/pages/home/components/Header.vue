<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      请输入城市/景点等名称</div>
    <div class="header-right">城市
      <span class="iconfont">&#xe627;</span>
    </div>
  </div>
</template>
<script>
/* eslint-disable */
export default {
  name: "Header"
};
</script>
<style lang='stylus' scoped>
@import '~styles/varibles.styl';
.header {
  display: flex;
  line-height: 0.86rem;
  background: $bgColor;
  color: #fff;

  .header-left {
    width: 0.64rem;
    float: left;
  }

  .header-input {
    flex: 1;
    height: 0.64rem;
    line-height: 0.64rem;
    color: #cccccc;
    background-color: #ffffff;
    border-radius: 0.1rem;
    padding-left: .1rem;
    margin-left: .1rem;
    margin-top: 0.12rem;
    margin-left: 0.1rem;
    margin-right: 0.1rem;
  }

  .header-right {
    float: right;
    width: 1.24rem;
  }
}
</style>
