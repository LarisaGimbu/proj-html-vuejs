<template>
  <div class="jumbotron d-flex justify-content-center align-items-center flex-column">
    
    <div class="todays-pick p-4 text-center">
      <div class="box-label p-2">TODAY'S PICK</div>
      <h1>Lorem ipsum dolor sit amet consectetur.</h1>
      <p class="date">March 25, 2019</p>
    </div>
    <div class="container text-center foodies">
      <h5>FOODIE JOURNAL</h5>
      <div>CARD</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Jumbotron'
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';

.jumbotron{
  width: 100%;
  min-height: 80vh;
  background-image: url("../assets/img/single-post-img3-1200x790.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  .todays-pick{
    position: relative;
    width: 500px;
    background-color: white;
    .box-label{
      position: absolute;
      top: -15px;
      left: 50%;
      transform: translate(-50%);
      width: 30%;
      background-color: $primary-color;
      font-size: 0.8rem;
      color: white;
      border-radius: 10px;
      box-shadow: 1px 1px 10px #AFAFAF;
    }
    .date{
      color: $grey-text;
    }
    .foodies{
      background-color: white;
    }
    
  }
}

</style>