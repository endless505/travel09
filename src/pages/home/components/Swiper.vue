<template>
  <div class="wrapper">
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
export default{
  name: 'HomeSwiper',
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: 1001,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/31/da037478f37cf202.jpg_750x200_a02cf862.jpg'
      }, {
        id: 1002,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/87/534cf2e0a71fff02.jpg_750x200_5c778719.jpg'
      }]
    }
  }
}
</script>

<style scoped>
  .swiper_img{
    width: 100%;
  }
  .wrapper >>> .swiper-pagination-bullet-active{
    background: #fff !important
  }
</style>
