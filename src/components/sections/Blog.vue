<template>
  <section id="blog">
    <div class="container">
      <div class="row space-between m-b-25 center-align">
        <div class="col-30 fs-22 text-black">Featured playlists</div>
        <a href="#" class="col-30 text-right text-black">View all videos <i class="fa-solid fa-angle-right"></i></a>
      </div>
      <div class="row space-between">
        <Article 
        v-for="(article,index) in articles" 
        :key=index
        :title=article.title
        :author=article.author
        :img=article.img
        :date=article.date
        :cathegory=article.cathegory />
      </div>
    </div>    
  </section>
</template>

<script>
import Article from "../commons/Article.vue"

export default {
    name: "Blog",
    components:{
      Article
    },
    data(){
      return{
        articles:[
          {
            title:"The best protein shake",
            author:"admin",
            img: "blog4-2x.jpg",
            date: "February 10th, 2022",
            cathegory: "Gym"
          },
          {
            title:"Ultimate cardio workout",
            author:"admin",
            img: "blog1-2x.jpg",
            date: "February 10th, 2022",
            cathegory: "Gym"
          },
          {
            title:"New juices available now",
            author:"admin",
            img: "blog3-2x.jpg",
            date: "February 10th, 2022",
            cathegory: "Gym"
          }
        ]
      }
    }
}
</script>

<style scoped>
  #blog{
    padding:100px;
  }

  .container a{
    margin:0;
  }

</style>