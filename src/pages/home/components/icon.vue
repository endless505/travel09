<template>
    <div class="icons">
      <swiper :options = ' swiperOption '>
        <swiper-slide v-for="(page, index) of pages" :key="index">
          <div class="icon" v-for="item in page" :key="item.id">
            <div class="icon_img">
                <img :src="item.url" class="icon_img_style">
            </div>
            <p class="icon_desc">{{item.desc}}</p>
          </div>
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
      
      
    </div>
</template>

<script>
export default {
  name: "HomeIcon",
  data: function() {
    return {
      swiperOption: {
        pagination: {
          el: ".swiper-pagination"
        },
        loop: true
      },
      iconlist: [
        {
          id: "1",
          url:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: "2",
          url:
            "http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png",
          desc: "泡温泉"
        },
        {
          id: "3",
          url:
            "http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
          desc: "成都必游"
        },
        {
          id: "4",
          url:
            "http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png",
          desc: "川剧变脸"
        },
        {
          id: "5",
          url:
            "https://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png",
          desc: "打卡圣地"
        },
        {
          id: "6",
          url:
            "http://img1.qunarzz.com/piao/fusion/1803/ea/01d081dacb03cc02.png",
          desc: "赏秋色"
        },
        {
          id: "7",
          url:
            "http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png",
          desc: "一日游"
        },
        {
          id: "8",
          url:
            "http://img1.qunarzz.com/piao/fusion/1803/54/35899492b1302802.png",
          desc: "成都熊猫基地"
        },
        {
          id: "9",
          url:
            "http://img1.qunarzz.com/piao/fusion/1805/57/1e29afd06f881102.png",
          desc: "稻城亚丁"
        }
      ]
    };
  },
  computed: {
    pages: function() {
      const pages = [];
      this.iconlist.forEach(function(item, index) {
        const page = Math.floor(index / 8);
        if (!pages[page]) {
          pages[page] = [];
        }
        pages[page].push(item);
      });
      return pages;
    }
  }
};
</script>

<style scoped>
.icons {
  width: 100%;
  height: 10px;
  padding-bottom: 50%;
  margin-top: 0.22rem;
}
.icon {
  width: 25%;
  padding-bottom: 25%;
  float: left;
  position: relative;
}
img {
  width: 70%;
}
.icon_img {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0.44rem;
}
.icon_img_style {
  width: 80%;
  display: table;
  margin: 0 auto;
}
.icon_desc {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: 0.44rem;
  line-height: 0.44rem;
  text-align: center;
}
.icons > .swiper-pagination-bullet-active {
  background: #abcdef !important;
}
</style>
