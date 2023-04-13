<template lang="">
    <footer>
        <div class="foot container d-flex justify-content-start align-items-center">
            <div class="links d-flex gap-5">
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
    </footer>
  </template>
  <script>
  import {footerLinks} from '../assets/data/data'
  export default {
    name : "FooterApp",
    data(){
    return {
      foots : footerLinks
    }
  }
  }
  </script>
  <style lang="scss" scoped>
    footer{
        height: 45vh;
        background-image: url(../assets/img/footer-bg.jpg);
        background-size:cover;
    }

    .foot{
        height:100%;
        overflow: hidden;
        position:relative;
    }

    .links{
        height: 80%;
    }
    .logo{
        position:absolute;
        height: 150%;
        right:0;
    }

    h1{
        color:white;
    }

    a{
        color:gray;
        font-size: 1.4rem;
        &:hover{
            color:blue;
        }
    }
  </style>