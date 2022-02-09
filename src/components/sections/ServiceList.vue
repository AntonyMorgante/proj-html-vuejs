<template>
  <section id="services">
    <div class="container up-100">
      <div class="row">
        <Service 
        v-for="(service,index) in services" 
        :key=index
        :title=service.title
        :disclaimer=service.disclaimer
        :img=service.img />
      </div>
      <div class="quote-container">
        <h2>"How you respond to the challenge in the second half will determine what you become after the game, whether you are a winner or a loser."</h2>
        <Waves />
        <Author :name=author.name :city=author.city :img=author.img />
      </div>
    </div>
  </section>
</template>

<script>
import Service from "../commons/Service.vue";
import Waves from "../commons/Waves.vue";
import Author from "../commons/Author.vue";

export default {
    name:"ServiceList",
    components:{
      Service,
      Waves,
      Author
    },
    data(){
      return{
        services:[
          {
          title:"Crossfit workout",
          disclaimer: "Push your limits",
          img: "service6-2x.jpg"
          },
          {
          title:"New gym apparel",
          disclaimer: "Look good, feel good",
          img: "box1-2x.jpg"
          },
          {
          title:"Team training",
          disclaimer: "Find a partner",
          img: "box3-2x.jpg"
          }
        ],
        author:{
          name:"Brad Johnson",
          city:"Las Vegas",
          img: "author.jpg"
        }
      }
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/globals.scss";

  #services{
    background: linear-gradient(135deg,blue, $reddish);
  }

  .up-100{
    position:relative;
    top:-100px;
  }

  .row{
    justify-content: space-around;
  }

  .quote-container{
    width:75%;
    margin:0 auto;
    padding:100px 0 50px;
  }

  h2{
    color:white;
    font-size:40px;
    text-align: center;
    line-height: 60px;
  }

  .waves{
    color:yellow;
    font-size:25px;
    text-align: center;
  }
</style>