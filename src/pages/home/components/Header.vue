<template>
  <div class="header">
    <div class="header_left">
      <div class="iconfont">&#xe6bc;</div>
    </div>
    <div class="header_input">
      <span class="iconfont">&#xe662;</span>
      <input type="text" placeholder="请输入你想要去的地点">
    </div>
    <div class="header_right">
      <span style="padding-left:5px;">成都</span>
      <span class="iconfont">&#xe6aa;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeHeader"
};
</script>

<style scoped>
.header {
  height: 0.88rem;
  line-height: 0.88rem;
  background: red;
  display: flex;
}
.header_left {
  float: left;
  width: 0.6rem;
}
.header_input {
  flex: 1;
  background: #fff;
  border-radius: 3px;
  height: 0.64rem;
  line-height: 0.64rem;
  margin-top: 0.12rem;
}
.header_right {
  float: right;
}
.iconfont {
  margin-left: 5px;
}
</style>
