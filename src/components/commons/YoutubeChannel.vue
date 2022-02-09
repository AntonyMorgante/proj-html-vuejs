<template>
  <div>
    <div class="channel-image">
      <img src="../../assets/unnamed.jpg" alt="">
    </div>
    <div class="channel-info">
      <div class="channel-name">
        Themefusion
      </div>
      <div>
        <a class="channel-link" href="#"><i class="fa-brands fa-youtube"></i>YouTube</a>
        <div class="subscr-count">999+</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    name:"YoutubeChannel"
}
</script>

<style lang="scss" scoped>

  .channel-image{
    display: inline-block;
    margin-right:10px;
  }

  .channel-info{
    display: inline-block;
    position:relative;
    top:-10px;
  }

  .channel-name{
    font-size:13px;
    height:30px;
    line-height: 30px;
  }

  .channel-link{
    display: inline-block;
    height:28px;
    background-color: red;
    font-size:12px;
    line-height:28px;
    padding: 0 10px;
    text-decoration: none;
    color:white;
    margin:0;  
  }

  .subscr-count{
    display: inline-block;
    height:26px;
    border:1px solid rgb(225,225,225);
    background-color:rgb(250,250,250);
    font-size:12px;
    line-height:26px;
    padding: 0 4px;
  }
</style>