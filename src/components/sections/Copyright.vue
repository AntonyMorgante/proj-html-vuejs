<template>
  <section id="copyright">
    <div class="text-center">
      <span>Copyright 2014-2022 |</span>
      <span>Avada Theme by <a href="#">ThemeFusion</a> |</span>
      <span>All rights reserved |</span>
      <span>Powered by <a href="#">WordPress</a></span>
    </div>
  </section>
</template>

<script>
export default {
    name: "Copyright"
}
</script>

<style lang="scss" scoped>
@import "../../assets/globals.scss";

  #copyright{
    padding: 40px 0;
    color: $secondary;
    font-size: 15px;
  }

  span{
    margin:0 2px;
  }

  a{
    margin:0;
    color:white;
  }
</style>