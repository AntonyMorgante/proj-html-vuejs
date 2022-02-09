<template>
  <section id="videos">
    <div class="clearfix">
      <div class="left">
        <div class="left-container">
        <img src="../../assets/service15-2x.jpg" alt="">
        <PlayButton />          
        </div>
      </div>
      <div class="right">
        <div class="right-container">
          <p class="blue-text">Tune up your workouts</p>
          <p class="section-title">The best health & fitness advice online</p>
          <YoutubeChannel />
          <p class="fs-22">Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis quam magni odio porro eveniet illum tenetur.</p>
          <button class="red button"><i class="fa-brands fa-youtube"></i> Visit my Youtube channel</button>
        </div>
      </div>
    </div>
    <div class="container">
      <div class="row space-between m-b-25">
        <div class="col-30 fs-22">Featured playlists</div>
        <div class="col-30 text-right">View all videos <i class="fa-solid fa-angle-right"></i></div>
      </div>
      <div class="row space-between">
        <Playlist 
        v-for="(playlist,index) in playlists" 
        :key=index
        :name=playlist.name
        :description=playlist.description
        :img=playlist.img />
      </div>
    </div>
  </section>
</template>

<script>
import PlayButton from "../commons/PlayButton.vue";
import YoutubeChannel from "../commons/YoutubeChannel.vue";
import Playlist from "../commons/Playlist.vue"

export default {
    name : "Videos",
    components:{
      PlayButton,
      YoutubeChannel,
      Playlist
    },
    data(){
      return{
        playlists:[
          {
            name: "Thigs & glute workout",
            description: "Increase your mobility",
            img: "video2-2x.jpg"
          },
          {
            name: "Lift, firm & perk up",
            description: "Feel young again",
            img: "video7-2x.jpg"
          },
          {
            name: "Slim & trim your waist",
            description: "Shed those extra pounds",
            img: "video9-2x.jpg"
          },
        ]
      }
    }
}
</script>

<style lang="scss">
@import "../../assets/globals.scss";
  #videos .left,
  #videos .right{
    width:50%;
  }

  .left-container{
    position:relative;
    top:-50px;

    img{
      width:100%;
      max-height: 950px;
      border-bottom-right-radius: 50px;
    }

    .play-button{
      position:absolute;
      top:50%;
      left: 50%;
      transform: translate(-50%,-50%);
    }
  }

  .right-container{
    padding:150px;
    
    .blue-text{
      color: $primary;
      font-size:30px;
    }

    .section-title{
      font-size: 60px;
      margin: 25px 0;
      color:black
    }

  }

.red{
  background-color: red;
  color:white;
}

.red.button{
  padding:20px 40px;
  font-size:16px;
}

.red.button:hover{
  background-color: $sienna;
}
</style>