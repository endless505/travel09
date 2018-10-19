<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <HomeIcon></HomeIcon>
  </div>
</template>

<script>
import HomeHeader from "./components/Header";
import HomeSwiper from "./components/Swiper";
import HomeIcon from "./components/icon";
export default {
  name: "Home",
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcon
  }
};
</script>

<style scoped>
</style>
