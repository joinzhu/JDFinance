<template lang="html">
  <a :class="[btnClass,cname]">
    <slot>去做任务</slot>
  </a>
</template>

<script>
export default {
  props:{
    cname:{
      type: String,
      default:""
    }
  },
  data(){
    return {
      btnClass:'btn',
    }
  },

}
</script>

<style lang="scss">
  @import "../css/element.scss";
  .btn{
    @include btn;
  }
</style>
