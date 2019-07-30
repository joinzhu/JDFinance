<template lang="html">
  <Panel :title="'保险保障'" :class="$style.panel">
    <Slider :swiperOption="swiperOption" :swiperSlides="swiperSlides" :cname="$style.slider"></Slider>
  </Panel>
</template>

<script>
import Panel from "../../component/panel.vue"
import Slider from "../../component/slider.vue"
export default {
  components:{
    Slider,
    Panel,
  },
  data(){
    return {
      swiperOption:{
        autoplay:false,
        loop:false,
        slidesPerView: 3,
        spaceBetween: 30,
        freeMode: true,
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        }
      },
      swiperSlides:[
        {
          href:'home1',
          src:'//img12.360buyimg.com/jrpmobile/jfs/t1/19965/4/1946/28370/5c18958aE9e8a930d/9810bed7979e6bd5.jpg?width=210&height=260'
        },
        {
          href:'home2',
          src:'//img12.360buyimg.com/jrpmobile/jfs/t1/27283/39/2034/26756/5c1895b5Ecbfdf7ed/6a0755f1f40e2eb9.jpg?width=210&height=260'
        },
        {
          href:'home3',
          src:'//img12.360buyimg.com/jrpmobile/jfs/t1/27014/35/2022/24897/5c1895d9Ef095679a/c0918d244bbfb2e5.jpg?width=210&height=260'
        }
      ]
    }
  }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel{
  @include panel;
  .slider{
    a{
      img{
        width:100%;
      }
    }
  }
}
</style>
