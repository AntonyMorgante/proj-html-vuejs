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
        DailyContent
    }
}
</script>

<style>

</style>