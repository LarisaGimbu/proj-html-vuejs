<template>
  <div class="farm container pt-5 pb-5 ">
    <div class="farm-title d-flex justify-content-between">
      <h3>FARM TO TABLE</h3>
      <button type="button" class="btn btn-danger my-button">READ OUR BLOG</button>
    </div>

    <p class="grey-text">Lorem ipsum dolor, sit amet consectetur adipisicing elit. <br/> Quam mollitia nam dignissimos facilis voluptatibus.</p>
    
    <div class="farm-content d-flex justify-content-between">
      <div class="farm-cards">
        <FarmCard />
        <div class="d-flex flex-wrap justify-content-between">
          <FoodCard v-for="card in 6" :key="card" />
        </div>

        <button type="button" class=" loader btn btn-outline-dark mt-5">LOAD MORE POSTS</button>
      </div>  

      <FarmAside />
    </div>
  </div>
</template>

<script>
import FarmCard from './FarmCard.vue'
import FoodCard from './FoodCard.vue'
import FarmAside from './FarmAside.vue'

export default {
  name: 'Farm',
  components:{
    FarmCard,
    FoodCard,
    FarmAside
  }
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';
@import '../assets/style/utilities.scss';

.farm-cards{
  width: 68%;
  .loader{
    background-color: #EDEDE7;
    width: 100%;
    border: none;

  }
}


</style>