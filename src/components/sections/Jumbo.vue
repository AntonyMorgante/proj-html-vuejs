<template>
  <section id="jumbo">
    <div class="container">
      <div class="row center-align">
        <div class="col-70">
          <p class="red-text">Certified fitness professional</p>
          <h1>Take control of your health</h1>
          <Waves />
          <p class="paragraph">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. 
          </p>
          <div>
            <button class="blue button"><i class="fa-brands fa-youtube"></i> Visit my Youtube channel</button>
            <button class="transparent button">Buy Avada today</button>
          </div>
        </div>
        <div class="col-30">
          <PlayButton />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import PlayButton from "../commons/PlayButton.vue";
import Waves from "../commons/Waves.vue"

export default {
    name:"Jumbo",
    components:{
      PlayButton,
      Waves
    }
}
</script>

<style>

</style>

<style lang="scss">
@import "../../assets/globals.scss";

  #jumbo{
    background-image: url("../../assets/jumbo-background.jpg");
    background-size: cover;
    padding-bottom:100px;
    position:relative;
    box-shadow: inset 900px 0px 60px -10px $dark;
  }

  #jumbo .row{
    display: flex;
    min-height: 600px;
  }

  .col-70{
    flex-basis:70%;
    z-index:3;

    .red-text{
      color:$reddish;
      font-size:25px;
    }

    h1{
      color:white;
      font-size: 60px;
      margin: 20px 0;
    }

    .paragraph{
      font-size:23px;
      color: $secondary;
      margin: 30px 0;
    }

    .transparent.button{
    border:1px solid white;
    padding: 15px 25px;
    border-radius:25px;
    background-color: transparent;
    color:white;
    transition: background-color 0.2s, color 0.2s;
    
    &:hover{
      background-color: white;
      color:black;
    }
    }
  }

  .waves{
    color:yellow;
    font-size:25px;
  }

  .col-30{
    flex-basis: 30%;
  }
</style>