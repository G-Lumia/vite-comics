<template lang="">
  <header class="d-flex container justify-content-between align-items-center my-0">
    <img src="../assets/img/dc-logo.png" alt="dc logo">
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
  height:15vh;
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
    position: relative;
    &:hover:after{
      position: absolute;
      content: "";
      left:0;
      bottom:0;
      width:100%;
      height:8px;
      background-color: #0C7CEC
  }
}
</style>