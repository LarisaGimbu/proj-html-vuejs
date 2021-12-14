<template>
  <div class="farm-card">
    <img src="../assets/img/single-post-img3.jpg" alt="">
    <div class="farm-content">
      <h5>Lorem ipsum dolor sit amet consectetur</h5>
      <p class="subtitle grey-text">Lorem ipsum dolor sit amet, consectetur</p>
      <div class="d-flex">
        <span class="points" v-for="punto in 120" :key="punto">.</span>
      </div>
      <p class="grey-text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ullam modi dicta, inventore eos quae rem eius veritatis quis suscipit autem eaque deserunt error ab cupiditate natus voluptates dolorum, minus saepe! </p>
      <a class="grey-text pt-5 pb-5" href="#">Read More ></a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FarmCard'
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';
@import '../assets/style/utilities.scss';

.farm-card{
  width: 100%;
  background-color: white;
  img{
    width: 100%;
  }
  .farm-content{
    width: 90%;
    margin: 0 auto;
    padding: 30px 0 30px 0;
    a{
      text-decoration: none;
    }
  }
}
</style>