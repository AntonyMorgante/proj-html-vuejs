<template>
  <div class="form">
    <input type="text" placeholder="Insert your email...*">
    <button class="blue button">Subscribe</button>
  </div>
</template>

<script>
export default {
    name: "MailForm"
}
</script>

<style lang="scss" scoped>
  .form{
    margin: 50px 0;
  }

  input{
    padding: 17px 400px 17px 20px;
    border-radius:30px;
    font-size:16px;
  }

  .blue.button{
    padding: 17px 100px;
  }
</style>