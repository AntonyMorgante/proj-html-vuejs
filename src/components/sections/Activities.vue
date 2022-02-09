<template>
  <section id="activities">
    <div class="container">
      <div class="row space-between">
        <Activity 
        v-for="(activity,index) in activities" 
        :key=index
        :symbol=activity.symbol
        :name=activity.name
        :disclaimer=activity.disclaimer
        :description=activity.description
        :url=activity.url
        :urlText=activity.urlText />      
      </div>
    </div>
  </section>
</template>

<script>
import Activity from "../commons/Activity.vue"

export default {
    name: "Activities",
    components:{
      Activity
    },
    data(){
      return{
        activities:[
          {
            symbol:"fa-solid fa-people-arrows-left-right",
            name:"Team training",
            disclaimer: "Find a partner",
            description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Totam praesentium laudantium, modi quod optio sint beatae enim voluptatem.",
            url:"#",
            urlText: "Find a partner"
          },
          {
            symbol:"fa-solid fa-dumbbell",
            name:"Crossfit workout",
            disclaimer: "Push your limits",
            description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit.  Officiis sed excepturi aspernatur consequuntur esse cumque nesciunt eveniet.",
            url:"#",
            urlText: "Learn about crossfit"
          },
          {
            symbol:"fa-solid fa-arrow-down-wide-short",
            name:"Weight loss plan",
            disclaimer: "Shed those pounds",
            description: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Temporibus, magni non facilis excepturi quo adipisci laudantium corporis asperiores.",
            url:"#",
            urlText: "Schedule a workout"
          },
        ]
      }
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/globals.scss";

  #activities{
    background-color: $dark;
    padding:100px;
  }
</style>