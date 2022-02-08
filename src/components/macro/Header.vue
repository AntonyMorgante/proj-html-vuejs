<template>
  <header>
      <div class="container clearfix">
          <div class="left">
              <Logo />
          </div>
          <div class="right">
              <Navbar />
              <button>Schedule a workout</button>
              <Actions />
          </div>
      </div>
  </header>
</template>

<script>
import Logo from "../commons/Logo.vue"
import Navbar from "../commons/Navbar.vue"
import Actions from "../commons/Actions.vue"

export default {
    name:"Header",
    components:{
        Logo,
        Navbar,
        Actions
    }
}
</script>

<style>
    .container{
        max-width:1170px;
        margin:0 auto;
    }

    .clearfix::after{
        content: "";
        display: table;
        clear: both;
    }
</style>