<template>
  <main>
      <Jumbo />
      <Services />
      <Videos />
      <MailingList />
      <Blog />
      <Store />
      <Partners />
      <DailyContent />
  </main>
</template>

<script>
import Jumbo from "../sections/Jumbo.vue"
import Services from "../sections/Services.vue"
import Videos from "../sections/Videos.vue"
import MailingList from "../sections/MailingList.vue"
import Blog from "../sections/Blog.vue"
import Store from "../sections/Store.vue"
import Partners from "../sections/Partners.vue"
import DailyContent from "../sections/DailyContent.vue"

export default {
    name: "Main",
    components:{
        Jumbo,
        Services,
        Videos,
        MailingList,
        Blog,
        Store,
        Partners,
        DailyContent
    }
}
</script>

<style>

</style>