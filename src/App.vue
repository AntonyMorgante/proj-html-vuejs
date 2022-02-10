<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/macro/Header.vue"
import Main from "./components/macro/Main.vue"
import Footer from "./components/macro/Footer.vue"


export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import "./assets/globals.scss";

body{
  box-sizing: border-box;
  margin:0;
  padding:0;
}

#app {
  font-family: Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.container{
  max-width:1370px;
}

.row{
  display: flex;
}

.space-between{
  justify-content: space-between;
}

.center-align{
  align-items: center;
}

.col-70{
  flex-basis:70%;
  z-index:3;
}

.text-center{
  text-align: center;
}

.text-right{
  text-align: right;
}

h1{
  color:white;
  font-size: 60px;
  margin: 20px 0;
}

.button{
  border:none;
  padding: 15px 25px;
  border-radius:25px;
}

.blue.button{
    background-color: $primary;
    color:white;
    margin: 0 15px;
    transition: background-color 0.2s;

    &:hover{
        background-color: $sienna;
    }
}

  .red-text{
    color:$reddish;
    font-size:25px;
  }

.m-b-25{
  margin-bottom: 25px;
}

.fs-22{
  font-size: 22px;
}

.text-black{
  color:black;
}
</style>
