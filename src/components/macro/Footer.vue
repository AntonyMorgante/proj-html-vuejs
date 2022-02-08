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

<style>

</style>