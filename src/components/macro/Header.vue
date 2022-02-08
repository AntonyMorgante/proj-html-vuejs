<template>
  <header>
      <div class="container clearfix">
          <div class="left">
              <Logo />
          </div>
          <div class="right">
              <Navbar />
              <button class="blue-button">Schedule a workout</button>
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

<style lang="scss">
@import "../../assets/globals.scss";

    header{
        background-color: $dark;
        padding: 20px;
    }

    .container{
        max-width:1370px;
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

    .blue-button{
        border:none;
        padding: 15px 25px;
        border-radius:25px;
        background-color: $primary;
        color:white;
        margin: 0 15px;
        transition: background-color 0.2s;

        &:hover{
            background-color: $reddish;
        }
    }
    
</style>