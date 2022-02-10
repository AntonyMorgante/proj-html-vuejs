<template>
  <p>
    <a :href="url"><i class="fa-solid fa-angle-right"></i> {{title}}</a>
  </p>
</template>

<script>
export default {
    name:"Post",
    props:{
        title:String,
        url:String
    }
}
</script>

<style lang="scss" scoped>
  p{
    margin:20px;
  }

  a{
    color:white;
    font-size:18px;
  }
</style>