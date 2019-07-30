<template lang="html">
  <article :class="$style.hslider">
    <Slider :swiperSlides="swiperSlides" :cname="$style.slider"></Slider>
    <section :class="$style.list">
      <div :class="$style.enter" v-for="enter in enters" :key="enter.img">
        <router-link :to="{ name: enter.href }">
          <img :src="enter.img" :alt="enter.title">
          <p>{{enter.title}}</p>
        </router-link>
      </div>
    </section>
  </article>
</template>

<script>
import Slider from "../../component/slider.vue"
export default {
  components:{
    Slider
  },
  data(){
    return {
      swiperSlides:[
        {
          src:'//img12.360buyimg.com/jrpmobile/jfs/t1/52802/14/4027/212241/5d1b14f4Ed1748086/588363d90a40b28c.png?width=750&height=320',
          href:'home1'
        },{
          src:'//img12.360buyimg.com/jrpmobile/jfs/t1/54124/12/3394/140400/5d11e389Ee12d74f3/f3cba452b6470938.png?width=750&height=320',
          href:'home2'
        }
      ],
      enters:[
        {
          img: '//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132',
          href: 'home',
          title: '优惠券'
        },{
          img: '//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132',
          href: 'home',
          title: '领福利'
        },{
          img: '//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132',
          href: 'home',
          title: '抢钢镚'
        },{
          img: '//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135',
          href: 'home',
          title: '白条提额'
        },
      ]
    }
  }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.hslider{
  .slider{
    margin-top: 88px;
    img{
      width: 100%;
    }
  }
  .list{
    @include list(row);
    padding-top: 40px;
    padding-bottom: 20px;
    justify-content: space-around;
    a{
      text-decoration: none;
      color: #333;
      font-size: 26px;
      img{
        width: 90px;
        margin-bottom: 14px;
      }
    }
    .enter{
      text-align: center;
    }
  }
}

</style>
