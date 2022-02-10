<template>
  <footer>
      <Info />
      <Copyright />
  </footer>
</template>

<script>
import Info from "../sections/Info.vue"
import Copyright from "../sections/Copyright.vue"

export default {
    name: "footer",
    components:{
        Info,
        Copyright
    }
}
</script>

<style lang="scss">
@import "../../assets/globals.scss";
    footer{
        background-color: $dark;
        text-align: center;
        color:white;
    }
</style>