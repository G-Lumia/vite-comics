<template lang="">
  <main>
    <section class="jumbotron">
    </section>
    <section>
      <div class="d-flex justify-content-center py-5 px-5 row">
        <PropApp v-for="(comic, index) in comics" :key="index" :thumb="comic.thumb" :series="comic.series" 
        :price="comic.price" :type="comic.type"/>
      </div>
    </section>
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
  import {images} from '../assets/data/data';
  import comicsJson from '../assets/data/dc-comics.json' assert {type: 'json'};
  import PropApp from './PropApp.vue';
  export default {
    name : "MainApp",
    components : 
    {
      PropApp
    },
    data(){
      return {
        pack : images,
        comics : comicsJson
      }
    },
  }
</script>
<style lang="scss" scoped>
  main{
    height:45%;
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
    width:80px;
   }

   .jumbotron{
    width:100%;
    height:30vh;
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
    background-attachment: fixed;
   }
</style>