<template>
  <div class="activity">
    <div class="activity-container text-center">
      <div>
        <i class="symbol" :class="symbol"></i>
      </div>
      <div class="name">
        {{name}}
      </div>
      <div class="disclaimer">
        {{disclaimer}}
      </div>
      <div class="description">
        {{description}}
      </div>
      <div>
        <a class="url-text" :href="url">{{urlText}} <i class="fa-solid fa-angle-right"></i></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: "Activity",
    props:{
      symbol: String,
      name: String,
      disclaimer: String,
      description: String,
      url: String,
      urlText: String
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/globals.scss";

  .activity{
    flex-basis: 30%;
    border: 5px solid $primary;
    min-height:500px;
    border-radius: 5px;
  }

  .activity-container{
    padding:80px 50px;
  }

  .symbol{
    font-size:70px;
    color:white;
    margin: 30px;
  }

  .name{
    color:white;
    font-size:25px;
  }

  .disclaimer{
    color:yellow;
    font-size:22px;
    margin:10px 0 50px;
  }

  .description{
    color:rgb(225,225,225);
    font-size:18px;
    line-height: 30px;
    margin-bottom:30px;
  }

  .url-text{
    color:white;
    font-size: 18px;
  }
</style>