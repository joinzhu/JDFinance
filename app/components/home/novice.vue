<template lang="html">
  <Panel :title="'新手组件'" :class="$style.panel">
    <section :class="[$style.content,$style.flex]">
      <div :class="[$style.item1,'tac']">
        <router-link :to="{ name: 'home' }">
          <h2>下载APP<span class="red">送888元礼包</span></h2>
          <p>新手专家</p>
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t1/23337/6/15445/8974/5cb064c2E0cadac1d/c533bfe4da578fe7.png?width=90&height=90" alt="">
        </router-link>
      </div>
      <div :class="$style.item1">
        <ul>
          <li>
            <router-link :to="{ name: 'home' }" :class="$style.flex">
              <div>
                <p class="red">领128元新手...</p>
                <p>立即开通</p>
              </div>
              <div>
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t1/36242/13/119/12214/5cb06492E0c73a66f/a284f91242e27af1.png?width=90&height=90" alt="">
              </div>
            </router-link>
          </li>
          <li>
            <router-link :to="{ name: 'home' }" :class="$style.flex">
              <div>
                <p>打白条<span class="red">享免息</span></p>
                <p>立即开通享豪礼</p>
              </div>
              <div>
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t1/1216/39/659/4516/5b923b1cE5943d1c6/dabaf8b842f57eb9.png?width=90&height=90" alt="">
              </div>
            </router-link>
          </li>
        </ul>
      </div>
    </section>
  </Panel>
</template>

<script>
import Panel from "../../component/panel.vue"
export default {
  components:{
    Panel,
  }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.flex{
  @include flex(row);
  box-sizing: border-box;
}
.panel{
  @include panel;
  >h2{
    border-bottom: 1px solid #ddd;
  }
  .content{
    font-size: 28px;
    .item1{
      width: 50%;
    }
  }
}
</style>
