<template>
  <div class="playlist-card">
    <div class="image-container">
      <img :src="getUrl(img)" alt="">
      <PlayButton />
    </div>
    <div class="text-center">
      <a href="#" class="playlist-name text-black">{{name}}</a>
      <p class="playlist-description">{{description}}</p>
    </div>
  </div>
</template>

<script>
import PlayButton from "./PlayButton.vue"

export default {
    name: "Playlist",
    components:{
      PlayButton
    },
    props:{
      name:String,
      description:String,
      img:String
    },
    methods:{
      getUrl(url){
        return require("../../assets/" + url)
      }
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/globals.scss";

  .playlist-card{
    flex-basis:30%;
    height:450px;
    background-size: cover;

    .image-container{
      position: relative;
      margin-bottom:25px;
    }

    img{
      width:100%;
      border-bottom-right-radius: 50px;   
    }

    .play-button{
    position:absolute;
    top:50%;
    left: 50%;
    transform: translate(-50%,-50%);
    width:60px;
    height:60px;
    }
  }

  .playlist-name{
    font-size:22px;
  }

  .playlist-description{
    color: $primary;
    margin:10px 0;
  }
</style>