<template lang="">
  <main>
    <div class="container py-5">
      <h1>
        content goes here
      </h1>
    </div>
    <section class="bg-primary py-5">
      <div class="container d-flex justify-content-between align-items-center">
        <div class="imageLink" v-for="(image, index) in pack" :key="index">
          <img :src=image.src alt={{image.title}}>
          <h3>
            {{image.title}}
          </h3>
        </div>
      </div>
    </section>
  </main>
</template>
<script>
import {images} from '../assets/data/data'
export default {
  name : "MainApp",
  data(){
    return {
      pack : images
    }
  }
}
</script>
<style lang="scss" scoped>
  main{
    background-color: black;
    height:fit-content;
  }
  h1,h3{
    color: white;
  }
  .imageLink{
    display: flex;
    align-items: center;
    gap:40px;
  }
   .imageLink img{
    width:50px;
   }
</style>