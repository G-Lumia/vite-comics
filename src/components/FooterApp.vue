<template lang="">
    <footer>
        <div class="foot d-flex align-items-center">
            <div class="container links d-flex gap-5 justify-content-start py-3">
                <div>
                    <div>
                        <h1 class="py-3">
                            {{foots[0].title}}
                        </h1>
                        <div class="d-flex flex-column justify-content-between gap-1">
                            <a v-for="(link, index) in foots[0].links" :key="index" :href="link.url">
                                {{link.title}}
                            </a>
                        </div>
                    </div>
                    <div>
                        <h1 class="py-3">
                            {{foots[1].title}}
                        </h1>
                        <div class="d-flex flex-column justify-content-between gap-1">
                            <a v-for="(link, index) in foots[1].links" :key="index" :href="link.url">
                                {{link.title}}
                            </a>
                        </div>
                    </div>
                </div>
                <div>
                    <h1 class="py-3">
                        {{foots[2].title}}
                    </h1>
                    <div class="d-flex flex-column justify-content-between gap-1">
                        <a v-for="(link, index) in foots[2].links" :key="index" :href="link.url">
                            {{link.title}}
                        </a>
                    </div>
                </div>
                <div>
                    <h1 class="py-3">
                        {{foots[3].title}}
                    </h1>
                    <div class="d-flex flex-column justify-content-between gap-1">
                        <a v-for="(link, index) in foots[3].links" :key="index" :href="link.url">
                            {{link.title}}
                        </a>
                    </div>
                </div>
            </div>
            <img class="logo" src="../assets/img/dc-logo-bg.png" alt="logo bg">
        </div>
        <div class="footerLinks py-5">
            <div class="container d-flex justify-content-between align-items-center">
                <div class="signUp border-primary p-3">
                    <a class="text-light" href="#">
                        Sign Up Now!    
                    </a>
                </div>
                <div class="d-flex gap-3 align-items-center">
                    <a href="#" class="text-primary"> Follow Us </a>
                    <div class="d-flex gap-2">
                        <img v-for="(image, index) in footsPics" :key="index" :src= image.src alt="image{{index}}">
                    </div>
                </div>
            </div>
        </div>
    </footer>
  </template>
  <script>
  import {footerLinks} from '../assets/data/data'
  import {footerImages} from '../assets/data/data'
  export default {
    name : "FooterApp",
    data(){
    return {
      foots : footerLinks,
      footsPics : footerImages
    }
  }
  }
  </script>
  <style lang="scss" scoped>
    footer{
        max-height:40vh; height: fit-content;
    }
    
    .foot{
        background-image: url(../assets/img/footer-bg.jpg);
        background-size:cover;
        height:80%;
        position:relative;
        overflow: hidden;
        
    }

    .links{
        height: 100%;
    }
    .logo{
        position:absolute;
        height: 130%;
        right:10%;
    }

    h1{
        color:white;
    }

    a{
        color:gray;
        font-size: 1.4rem;
        &:hover{
            color:lightblue;
        }
    }
    .footerLinks{
        background-color: darkgrey;
        height: 20%;
    }

    .footerLinks .container{
        height: 100%;
    }

    .footerLinks img{
        width:50px;
    }

    .footerLinks a{
        font-weight: bold;
        font-size: 2.4rem;
    }

    .signUp{
        border : 8px solid black;
    }
  </style>