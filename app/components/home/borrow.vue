<template lang="html">
  <Panel :title="'极速借贷'" :class="$style.panel">
    <section :class="$style.content">
      <img src="//m.jr.jd.com/spe/qyy/main/images/bg_seize.png" alt="">
    </section>
  </Panel>
</template>

<script>
import Panel from "../../component/panel.vue"
export default {
  components:{
    Panel
  }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel{
  @include panel;
  .content{

  }
}
</style>
