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
    header{
        background-color: #060606;
        padding: 20px;
    }

    .container{
        max-width:1170px;
        margin:0 auto;
    }

    .clearfix::after{
        content: "";
        display: table;
        clear: both;
    }

    .left{
        float:left;
        padding-top:3px;
    }

    .right{
        float: right;
    }

    button{
        border:none;
        padding: 15px 25px;
        border-radius:25px;
        background-color: #4154fe;
        color:white;
        margin: 0 15px;
    }
</style>