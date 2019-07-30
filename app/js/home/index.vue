<template lang="html">
    <div>
      <Heador></Heador>
      <Hslider></Hslider>
    </div>
</template>

<script>
import Heador from "../../components/home/header.vue"
import Hslider from "../../components/home/hslider.vue"
export default {
  components:{
    Heador,
    Hslider
  }
}
</script>

<style lang="scss" module>
  @import '../../css/reset.scss';
</style>
