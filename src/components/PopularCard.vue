<template>
  <div class="popular-card">
    <img src="../assets/img/Yogurt-Nan.jpg" alt="">
    <div class="popular-content">
      <h5>Lunch Favourite with Salad, Naan And Beans</h5>
      <p class="subtitle grey-text">Bakery, Featured, Healthy, Latest Recipes, Staff Picks</p>
      <div class="d-flex">
        <span class="points" v-for="punto in 120" :key="punto">.</span>
      </div>
      <p class="grey-text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ullam modi dicta, inventore eos quae rem eius veritatis quis suscipit autem eaque deserunt error ab cupiditate natus voluptates dolorum, minus saepe! Lorem ipsum dolor sit, amet consectetur adipisicing elit. Amet libero non blanditiis minus saepe! Lorem ipsum dolor sit, amet consectetur adipisicing elit. Amet libero non blanditiis</p>
      <button type="button" class="btn btn-danger my-button">LEARN MORE</button>
    </div>
  </div>
</template>

<script>
export default {
  name:'PopularCard'
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';
@import '../assets/style/utilities.scss';

.popular-card{
  width: 48%;
  background-color: white;
  img{
    width: 100%;
  }
  .popular-content{
    width: 90%;
    margin: 0 auto;
    padding: 30px 0 30px 0;
  }
}
</style>