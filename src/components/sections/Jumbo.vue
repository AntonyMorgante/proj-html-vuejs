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

<style lang="scss" scoped>
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
    .paragraph{
      font-size:23px;
      color: $secondary;
      margin: 30px 0;
    } 
  }

  .blue.button,
  .transparent.button{
    margin-left:0;
    padding:18px 40px;
  }
</style>