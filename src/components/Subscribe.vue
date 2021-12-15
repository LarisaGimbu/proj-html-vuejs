<template>
  <div class="subscribe d-flex flex-column justify-content-center align-items-center">
    <div class="description text-center">
      <h2>Subscribe and Receive A Free eBook</h2>
      <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. <br/> Quam mollitia</p>
    </div>

    <div class="input-group input-container mb-3">
      <input type="text" class="form-control me-4 email-input" placeholder="Insert your email ...*" aria-label="Recipient's username" aria-describedby="button-addon2">
      <button class="btn btn-outline-secondary my-button" type="button" id="button-addon2">SUBSCRIBE</button>
    </div>
    <p class="text-center">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
  </div>
</template>

<script>
export default {
  name: 'Subscribe'
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';
@import '../assets/style/utilities.scss';

.subscribe{
  width: 100%;
  height: 70vh;
  background-color: white;
  background-image: url('../assets/img/subscribe-sec-bg.png');
  background-size: cover;
  .input-container{
    max-width: 500px;
    margin: 0 auto;
    .email-input{
      border-radius: 0.25rem !important;
    }
  }
}
</style>