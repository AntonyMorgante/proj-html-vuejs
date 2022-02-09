<template>
    <div class="play-button">
        <i class="fas fa-play play-button-icon"></i>
    </div>
</template>

<script>
export default {
    name:"PlayButton"
}
</script>

<style lang="scss" scoped>
@import "../../assets/globals.scss";

    .play-button{
        display: inline-block;
        width:90px;
        height:90px;
        background-color:white;
        border-radius:50%;
    }

    .play-button-icon{
        color:$primary;
        font-size:20px;
        position:relative;
        top:50%;
        left:50%;
        transform: translate(-50%,-50%);
    }
</style>