<template>
  <div class="partner-card text-center">
    <img :src="getUrl(img)" alt="">
    <Waves />
    <p class="paragraph">{{description}}</p>
    <a class="text-black redirect" :href="redirection">{{disclaimer}} <i class="fa-solid fa-angle-right"></i></a>
  </div>
</template>

<script>
import Waves from "../commons/Waves.vue"

export default {
    name:"Partner",
    props:{
      img:String,
      description:String,
      redirection:String,
      disclaimer:String
    },
    components:{
      Waves
    },
    methods:{
      getUrl(url){
        return require("../../assets/" + url);
      }
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/globals.scss";

  .partner-card{
    flex-basis:20%;

    img{
      width:60%;
      margin-bottom: 15px;
    }
  }

  .waves{
    color:$primary;
    font-size:20px;
  }
  
  .paragraph{
    font-size:18px;
    line-height: 25px;
    margin-bottom: 40px;
  }

  .redirect{
    font-size: 18px;
  }
</style>