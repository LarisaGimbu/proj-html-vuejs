<template>
  <div class="contacts pt-5 pb-5">
    <div class="container d-flex justify-content-between">
      <div class="logo pe-5">
        <img src="../assets/img/avada-food-logo-mob.png" alt="">
        <p>SOCIAL</p>
      </div>
    
      <div class="pe-5">
        elenco navbar
      </div>
      <div class="pe-5">
        <h5>CONTACT</h5>
        <p>location</p>
        <p>tel</p>
        <p>mail</p>
      </div>
      <div>
        <h5>GET OUR APP!</h5>
        <p>Google Play</p>
        <p>App Store</p>
      </div>
    </div>

  </div>
</template>

<script>
export default {
name: 'Contacts'
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';
@import '../assets/style/utilities.scss';


.contacts{
  background-color: white;
  h5{
    color: $primary-color;
  }
}
</style>