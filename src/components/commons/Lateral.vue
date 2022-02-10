<template>
  <div class="text-center lateral-card">
    <a :href="url">
      <i :class="icon"></i>
      <p>{{text}}</p>
    </a>
  </div>
</template>

<script>
export default {
    name:"Lateral",
    props:{
      icon: String,
      text: String,
      url: String,
    }
}
</script>

<style lang="scss" scoped>
  .lateral-card{
    margin-bottom:10px;
    background-color:white;
    display: inline-block;
    width:70px;
    height:50px;
    padding: 10px 0;
    border-radius:5px;
    border:1px solid black;
  }

  a{
    margin:0;
    color:rgb(75,75,75);
    font-size: 25px;

    p{
      font-size:14px;
      margin:5px;
    }
  }
</style>