<template>
    <div class="row center-align">
        <img :src="getImg(img)" alt="">
        <div class="author">{{name}}</div>
        <div class="author-city">{{city}}</div>
    </div>
</template>

<script>
export default {
    name:"Author",
    props:{
        img: String,
        name: String,
        city: String
    },
    methods:{
        getImg(url){
            return require("../../assets/" + url)
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/globals.scss";
    .row{
        width: 33%;
        margin: 0 auto;
        justify-content: space-between;
    }

    img{
        width: 60px;
        height:60px;
        border-radius: 50%;
    }

    .author{
        color:white;
        font-size:20px
    }

    .author-city{
        color: $secondary;
        font-size:20px
    }
</style>