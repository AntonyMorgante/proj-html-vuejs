<template>
  <main>
      <Jumbo />
      <ServiceList />
      <Videos />
      <MailingList />
      <Activities />
      <Blog />
      <Store />
      <Partners />
      <DailyContent />
      <div class="laterals">
        <Lateral
        v-for="(offer,index) in laterals"
        :key=index
        :icon=offer.icon
        :text=offer.text
        :url=offer.url
        />
      </div>
  </main>
</template>

<script>
import Jumbo from "../sections/Jumbo.vue"
import ServiceList from "../sections/ServiceList.vue"
import Videos from "../sections/Videos.vue"
import MailingList from "../sections/MailingList.vue"
import Activities from "../sections/Activities.vue"
import Blog from "../sections/Blog.vue"
import Store from "../sections/Store.vue"
import Partners from "../sections/Partners.vue"
import DailyContent from "../sections/DailyContent.vue"
import Lateral from "../commons/Lateral.vue"

export default {
    name: "Main",
    components:{
        Jumbo,
        ServiceList,
        Videos,
        MailingList,
        Activities,
        Blog,
        Store,
        Partners,
        DailyContent,
        Lateral
    },
    data(){
        return{
            laterals:[
                {
                    name:"Demos",
                    icon:"fa-solid fa-floppy-disk",
                    text:"Demos",
                    url: "#"
                },
                {
                    name:"On sale",
                    icon:"fa-solid fa-magnifying-glass-dollar",
                    text:"On Sale",
                    url: "#"
                }
            ]
        }
    }
}
</script>

<style lang="scss">
    .laterals{
        z-index:99;
        display: flex;
        flex-direction: column;
        position:fixed;
        right:-5px;
        top: 200px;
    }
</style>