<template>
  <section id="daily-content">
    <div class="text-center">
      <PlayButton />
      <p class="title">Crossfit workout of the day</p>
      <p class="date">February 9th, 2022</p>
      <a href="#">View all videos <i class="fa-solid fa-arrow-right-long"></i></a>
    </div>
  </section>
</template>

<script>
import PlayButton from "../commons/PlayButton.vue"

export default {
    name: "DailyContent",
    components:{
      PlayButton
    }
}
</script>

<style lang="scss" scoped>
  #daily-content{
    background-image: linear-gradient(135deg, rgba(8, 37, 202, 0.7) 0%, rgba(19, 45, 192, 0.3) 40%, rgba(173, 15, 23, 0.7)100%), url("../../assets/banner14-2x.jpg");
    background-size: cover;
  }

  .text-center{
    backdrop-filter:contrast(150%) brightness(50%);
    padding:200px;
  }

  .title{
    font-size: 55px;
    color:white;
    margin: 25px 0;
  }

  .date{
    color:yellow;
    font-size:30px;
    margin-bottom:20px;
  }

  a{
    color:white;
    font-size: 18px;
  }

  .play-button{
    text-align: left;
  }
</style>