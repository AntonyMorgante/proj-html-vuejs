<template>
    <nav>
        <a v-for="(element,index) in navbar" 
        :key=index 
        :href="element.url">{{element.name}}</a>
    </nav>
</template>

<script>
export default {
    name: "Navbar",
    data(){
        return{
            navbar: [
                {
                    name: "Home",
                    url : "#home"
                },
                {
                    name: "Services",
                    url: "#services"
                },
                {
                    name: "About",
                    url: "#about"
                },
                {
                    name: "Videos",
                    url: "#videos"
                },
                {
                    name: "Blog",
                    url: "#blog"
                },
                {
                    name: "Store",
                    url: "#store"
                },
            ]
        }
    }
}
</script>

<style lang="scss">
@import "../../assets/globals.scss";

    nav{
        display: inline-block;
    }

    a{
        text-decoration: none;
        color:$secondary;
        margin: 20px;
    }

    nav a:first-of-type{
        color:white;
    }

    nav a:last-child::after{
        content:"new";
        margin-left:7px;
        padding:5px;
        color:black;
        background-color:yellow;
        font-size: 12px;
        border-radius: 2px;
        position:relative;
        top: -2px;
    }
</style>