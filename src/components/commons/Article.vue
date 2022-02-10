<template>
  <div class="article-card">
    <div>
      <img :src="getUrl(img)" alt="">
    </div>
    <p class="fs-22 text-black">{{title}}</p>
    <div class="row">
      <span>By <a class="text-black" href="#">{{author}}</a></span>
      <span>| {{date}} |</span>
      <span><a class="text-black" href="#">{{cathegory}}</a></span>
    </div>
  </div>
</template>

<script>
export default {
    name:"Article",
    props:{
      title: String,
      author:String,
      img: String,
      date: String,
      cathegory: String,
    },
    methods:{
      getUrl(url){
        return require("../../assets/" + url)
      }
    }
}
</script>

<style lang="scss">

  .article-card{
    flex-basis:30%;
    height:450px;

    img{
      width:100%;
    }

    p{
      margin:20px 20px 10px;
    }

    .row{
      margin-left:20px;
    }

    a{
      margin:0;
    }

    span{
      margin:0 5px;
    }

  }  


</style>