<template>
  <div class="wraper">
    <swiper :options="swiperOption">
    <!-- slides -->
      <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper_img" :src="item.imgUrl" alt="">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
export default {
  name: "HomeSwiper",
  data: function() {
    return {
      swiperOption: {
        pagination: {
          el: ".swiper-pagination"
        }
      },
      swiperList: [
        {
          id: "1001",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1809/91/836652a03cc5f802.jpg_890x330_628a9416.jpg"
        },
        {
          id: "1002",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1810/fb/030e309242deb002.png_890x330_e904912c.png"
        },
        {
          id: "1003",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1810/27/73c955aefe37302.jpg_890x330_6961ae90.jpg"
        }
      ]
    };
  }
};
</script>

<style scoped>
.swiper_img {
  width: 100%;
}
.wraper >>> .swiper-pagination-bullet-active {
  background: #fff !important;
}
</style>
