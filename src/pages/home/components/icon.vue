<template>
    <div class="icons">
      <div class="icon" v-for="item in iconlist" :key="item.id">
        <div class="icon_img">
            <img :src="item.url" alt="q" class="icon_img_style">
        </div>
        <p class="icon_desc">{{item.desc}}</p>
      </div>
      
    </div>
</template>

<script>
export default {
  name: "HomeIcon",
  data: function() {
    return {
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
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: "3",
          url:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: "4",
          url:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: "5",
          url:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: "6",
          url:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: "7",
          url:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: "8",
          url:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        }
      ]
    };
  }
};
</script>

<style scoped>
.icons {
  width: 100%;
  height: 10px;
  padding-bottom: 50%;
  background-color: green;
}
.icon {
  width: 25%;
  padding-bottom: 25%;
  float: left;
  position: relative;
}
img {
  width: 80%;
}
.icon_img {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0.44rem;
}
.icon_img_style {
  width: 100%;
  display: bolck;
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
</style>
