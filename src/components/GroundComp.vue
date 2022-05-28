
<template>

  <div class="ground-comp"> 
    <header-cpm-comp/>
    <navi-comp/>
    <memo-comp/>
    <footer-comp/>
  </div>  
</template>

<script>
import FooterComp from './FooterComp.vue';
import HeaderCpmComp from './HeaderCpmComp.vue';
import NaviComp from './NaviComp.vue';
import MemoComp from './MemoComp.vue';

export default {
components: { FooterComp , MemoComp ,NaviComp,HeaderCpmComp },
}
</script>

<style scoped>
  @import "../css/style.css";
</style>

