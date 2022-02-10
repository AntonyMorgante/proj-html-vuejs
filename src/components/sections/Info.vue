<template>
  <section id="info">
    <div class="container">
      <div class="row space-between">
        <div class="col-30">
          <Logo />
          <p class="description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum nihil doloremque quibusdam neque saepe tenetur repudiandae vitae?</p>
          <div class="row justify-center">
            <Social
            v-for="(social, index) in socials"
            :key=index
            :icon=social.icon
            :url=social.url
            />
          </div>
        </div>
        <div class="col-30">
          <p class="title">Recent posts</p>
          <Post
          v-for="(post,index) in posts"
          :key=index
          :title=post.title
          :url=post.url
           />
        </div>
        <div class="col-30">
            <p class="title">Contact informations</p>
            <p class="address">4746 Tipple Road Michigan 48449</p>
            <p class="contact">Mobile: 1.800.000.0000
            <br>Email: info@your-company.com</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from "../commons/Logo.vue"
import Social from "../commons/Social.vue"
import Post from "../commons/Post.vue"

export default {
    name: "Info",
    components:{
      Logo,
      Social,
      Post
    },
    data(){
      return{
        socials:[
          {
            name: "Facebook",
            icon: "fa-brands fa-facebook-f",
            url: "#"
          },
          {
            name: "Twitter",
            icon: "fa-brands fa-twitter",
            url: "#"
          },
          {
            name: "Youtube",
            icon: "fa-brands fa-youtube",
            url: "#"
          },
          {
            name: "Instagram",
            icon: "fa-brands fa-instagram",
            url: "#"
          },
          {
            name: "Linkedin",
            icon: "fa-brands fa-linkedin-in",
            url: "#"
          }
        ],
        posts:[
          {
            title:"The best protein shake",
            url:"#"
          },
          {
            title:"Ultimate cardio workout",
            url:"#"
          },
          {
            title:"New juices available now",
            url:"#"
          },
          {
            title:"Tips to find training partners",
            url:"#"
          },
          {
            title:"20 best healthy recipes",
            url:"#"
          }
        ]
      }
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/globals.scss";

  #info{
    padding:150px 0 100px;
    border-bottom: 1px solid $secondary;
  }

  .justify-center{
    justify-content: center;
  }

  .title{
    text-transform: uppercase;
    font-size:20px;
    margin-top:0;
    margin-bottom:40px;
  }

  .description{
    color: rgb(200,200,200);
    font-size:18px;
    line-height: 30px;
  }

  .address{
    color: rgb(200,200,200);
    font-size:18px;
    margin-bottom:25px;
  }

  .contact{
    font-size:18px;
    line-height: 25px;
  }
</style>