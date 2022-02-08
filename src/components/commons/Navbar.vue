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

<style>
    nav{
        display: inline-block;
    }

    a{
        text-decoration: none;
        color:white;
        padding: 10px;
    }
</style>