<template>
  <section id="mailing-list">
    <div class="container">
      <div class="w-70">
        <p class="red-text">Join our mailing list today</p>
        <h1>Insider offers & flash sales in your inbox every week.</h1>
        <Waves />    
        <MailForm />    
        <p class="fs-22">Lorem ipsum dolor sit amet consectetur adipisicing elit. Nihil, exercitationem maiores rem cum saepe ipsum quia 
          temporibus.</p>
      </div>
    </div>
  </section>
</template>

<script>
import Waves from "../commons/Waves.vue";
import MailForm from "../commons/MailForm.vue";

export default {
    name:"MailingList",
    components:{
      Waves,
      MailForm
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/globals.scss";

  .w-70{
    max-width: 70%;
    padding:100px 50px;
  }

  h1{
    margin: 20px 0 40px;
  }

  #mailing-list{
    background-image: url("../../assets//banner1-2x.jpg");
    background-size: cover;
    min-height: 650px;
    box-shadow: inset 1000px 0px 100px 5px $dark;
  }
  
  .fs-22{
    color: $secondary;
    margin: 30px 0;
    line-height:35px;
  }
</style>