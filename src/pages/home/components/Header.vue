<template>
<div class="header">
    <div class="header_left">
      <div class="iconfont back_icon">&#xe624;</div>
    </div>
    <div class="header_input">
      <span class="iconfont">&#xe632;</span>
      输入城市/游玩/景点主题
    </div>
    <div class="header_right">
      城市
      <span class="iconfont">&#xe6aa;</span>
    </div>

</div>
</template>

<script>
export default{
  name: 'HomeHeader'
}
</script>

<style scoped>  
  .header{
    line-height: .86rem;
    display: flex;
    background-color: #00bcd4;
    color: #fff;
  }
  .header_left{width: .64rem;float: left;}
  .header_input{
    flex: 1;
    padding-left: .2rem;
    background: #fff;
    border-radius: .1rem;
    height: .64rem;
    line-height: .64rem;
    margin-top: .12rem;
    margin-left: .2rem;
    color: #ccc;
  }
  .back_icon{text-align: center;}
  .header_right{width: 1.24rem;float: right;text-align: center;}
</style>
