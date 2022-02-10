<template>
  <section id="store">
    <div class="container text-center">
      <div class="content-container">
        <p class="title">
          "I've failed over and over again in my life. And that is why I succeed."
        </p>
        <Waves />
        <p class="paragraph">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Eius repudiandae omnis ratione aliquid, dolores dicta assumenda maiores aliquam?
        </p>
        <button class="blue button">Buy Avada today <i class="fa-solid fa-angle-right"></i></button>
      </div>
    </div>
  </section>
</template>

<script>
import Waves from '../commons/Waves.vue'
export default {
  components: { Waves },
    name: "Store"
}
</script>

<style lang="scss" scoped>
@import "../../assets/globals.scss";

  #store{
    padding:100px;
    background-image: url("../../assets/banner2-2x.jpg");
    background-size: cover;
    min-height: 550px;
    box-shadow: inset 0 -150px 500px 100px rgb(2, 2, 14);
    color:white;
  }

  .content-container{
    width:70%;
    margin:0 auto;
  }

  .title{
    font-size:55px;
    margin: 80px 0 30px;
    line-height: 75px;
  }

  .paragraph{
    font-size: 25px;
    line-height: 35px;
    margin: 30px 0 35px;
  }

  .blue.button{
    font-size:16px;
    padding: 18px 40px;
  }
</style>