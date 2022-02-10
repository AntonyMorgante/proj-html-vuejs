<template>
  <div class="article-card">
    <div>
      <img :src="getUrl(img)" alt="">
    </div>
    <a href="#" class="fs-22 text-black">{{title}}</a>
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

<style lang="scss" scoped>

  .article-card{
    flex-basis:30%;
    height:450px;

    img{
      width:100%;
      margin-bottom:20px;
    }

    a.fs-22{
      padding-left:25px;
    }

    .row{
      margin:10px 20px;
    }

    a{
      margin:0;
    }

    span{
      margin:0 5px;
    }

  }  


</style>