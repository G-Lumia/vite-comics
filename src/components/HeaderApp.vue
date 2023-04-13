<template lang="">
  <header class="d-flex container justify-content-between align-items-center my-5">
    <div>
      <img src="../assets/img/dc-logo.png" alt="dc logo">
    </div>
    <div class="d-flex gap-5">
      <a v-for="(link, index) in navbar" :key="index" :href="link.url"> {{link.title}}</a>
    </div>
  </header>
</template>
<script>
import {links} from '../assets/data/data'
export default {
  name : "HeaderApp",
  data(){
    return {
      navbar : links
    }
  }
}
</script>
<style lang="scss" scoped>
header {
  height:10vh;
}
header div{
  height:100%;
}
img {
    width:150px;
}
a {
    color:gray;
    font-size: 1.6rem;
    height: 100%;
    display:flex;
    align-items: center;
    &:hover{
      color:cyan;
      border-bottom: 6px solid black;
    }
}
</style>