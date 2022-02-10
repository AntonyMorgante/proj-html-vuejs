<template>
  <a :href="url">
    <i class="icon" :class="icon"></i>
  </a>
</template>

<script>
export default {
    name:"Social",
    props:{
      name: String,
      icon: String,
      url: String
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/globals.scss";
  
  a{
    color:$sienna;
    margin:30px 10px;
    font-size:18px;
  }
</style>