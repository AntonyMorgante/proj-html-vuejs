<template>
  <a href="#" class="service-card" :style='{ backgroundImage: `url("${getUrl(img)}")`}'>
      <div class="description"> 
        <Waves />
        <p class="title">{{title}}</p>
        <p class="disclaimer">{{disclaimer}}</p>        
      </div>
  </a>
</template>

<script>
import Waves from "./Waves.vue";

export default {
    name:"Service",
    components:{
      Waves
    },
    props:{
      title: String,
      disclaimer: String,
      img: String
    },
    methods:{
      getUrl(url){
        return require("../../assets/" + url)
      }
    }
}
</script>

<style lang="scss" scoped>
  .service-card{
    flex-basis:30%;
    height:450px;
    background-size: cover;
    box-shadow: inset 0px -100px 150px black;
    border-bottom-right-radius: 50px;
    margin:0px;
  
    .description{
      position:relative;
      left:40px;
      top: 300px;
    }

    .waves{
      color:white;
      font-size:20px;
    }

    .title{
      color:white;
      font-size:30px;
      margin: 10px 0;
    }

    .disclaimer{
      color:yellow;
      font-size:22px;
      margin:10px 0;
    }
  }


</style>