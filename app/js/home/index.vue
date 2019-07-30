<template lang="html">
    <div>
      <Heador></Heador>
      <Hslider></Hslider>
      <Novice></Novice>
      <Borrow></Borrow>
      <Product></Product>
    </div>
</template>

<script>
import Heador from "../../components/home/header.vue"
import Hslider from "../../components/home/hslider.vue"
import Novice from "../../components/home/novice.vue"
import Borrow from "../../components/home/borrow.vue"
import Product from "../../components/home/product.vue"
export default {
  components:{
    Heador,
    Hslider,
    Novice,
    Borrow,
    Product,
  }
}
</script>
