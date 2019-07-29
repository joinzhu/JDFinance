<template lang="html">
  <section :class="cname">
    <swiper :options="swiperOption" :not-next-tick="swiperOption.notNextTick">
      <swiper-slide v-for="swiper in swiperSlides" :key="swiper.href">
        <router-link :to="{ name: swiper.href }">
          <img :src="swiper.src" alt="">
        </router-link>
      </swiper-slide>
      <div class="swiper-pagination" v-if="swiperOption.pagination"></div>
    </swiper>
  </section>
</template>

<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
  components:{
    swiper,
    swiperSlide
  },
  props:{
    cname:{
      type:String,
      default:''
    },
    swiperOption:{
      type:Object,
      default(){
        return {
          autoplay:true,
          loop:true,
          pagination: {
            el: '.swiper-pagination',
          },
          notNextTick:false
        }
      }
    },
    swiperSlides:{
      type:Array,
      default(){
        return []
      }
    }
  },

}
</script>

<style lang="scss">
@import "~swiper/dist/css/swiper.css";
</style>
