<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon_img">
            <img class="icon_img_style" :src="item.imgUrl" alt="">
          </div>
          <p class="icon_desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default{
  name: 'HomeIcons',
  data: function () {
    return {
      iconList: [{
        id: 1001,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '热门景点'
      }, {
        id: 1002,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: 1003,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: 1004,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: 1005,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: 1006,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: 1007,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: 1008,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/ea/01d081dacb03cc02.png',
        desc: '赏秋色'
      }, {
        id: 1009,
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        desc: '成都必游'
      }]
    }
  },
  computed: {
    pages: function () {
      const pages = []
      this.iconList.forEach(function (item, index) {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style scoped>
  .icons >>> .swiper-container{
    overflow: hidden;
    height: 0;width: 100%;
    padding-bottom: 50%;
    /* background-color: green; */
  }
  .icon{
    position: relative;
    overflow: hidden;
    float: left;
    height: 0;
    width: 25%;
    padding-bottom: 25%;
    /* background-color: red; */
  }
  .icon_img{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: .44rem;
    /* background-color: blue; */
    /* padding: .1rem; */
  }
  .icon_img_style{
    display: block;
    height: 100%;
    margin: 0 auto;
  }
  .icon_desc{
    position: absolute;
    bottom: 0;left: 0;right: 0;
    height: .44rem;
    line-height: .44rem;
    text-align: center;
    color: #333;
  }
</style>
