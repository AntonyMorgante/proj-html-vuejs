<template>
  <section id="partners">
    <div class="container">
      <div class="row space-between">
        <Partner
        v-for="(partner,index) in partners"
        :key=index
        :img=partner.img
        :description=partner.description
        :redirection=partner.redirection
        :disclaimer=partner.disclaimer
        />
      </div>
    </div>
  </section>
</template>

<script>
import Partner from "../commons/Partner.vue"

export default {
    name:"Partners",
    components:{
      Partner
    },
    data(){
      return{
        partners: [
          {
            name:"Yoga Studio",
            img: "sponsor-1-2x.png",
            description:"Duis ut hendrerit mauris. Nulla eget ultrices diam. Ut mattis placerat erat et cursus.",
            disclaimer:"Visit Yoga Studio",
            redirection:"#"
          },
          {
            name:"Fitness Center",
            img: "sponsor-2-2x.png",
            description:"Cras vehicula porta mattis. Curabitur tortor nulla, fermentum nec nulla et, sollicitudin tempus.",
            disclaimer:"Join fitness center",
            redirection:"#"
          },
          {
            name:"Fitness Club",
            img: "sponsor-3-2x.png",
            description:"Etiam ullamcorper, velit ut laoreet, purus lorem euismod odio, justo risus porttitor urna.",
            disclaimer:"Learn about FC",
            redirection:"#"
          },
          {
            name:"Power Gym",
            img: "sponsor-4-2x.png",
            description:"Proin massa purus, pulvinar in nisl eu, tincidunt bibendum libero. Consectetur, sapien a tristique.",
            disclaimer:"Visit Power Gym",
            redirection:"#"
          }
        ]
      }
    }
}
</script>

<style lang="scss" scoped>
  #partners{
    padding:100px;
  }
</style>