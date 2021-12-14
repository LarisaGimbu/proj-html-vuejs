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

      <aside>
        <div class="latest-recipes-box">
          <!-- <img src="../assets/img/ad-bg.jpg" alt=""> -->
          <h4 class="latest-recipes-text text-center">VIEW OUR LATEST RECIPES</h4>
        </div>
        <div class="singapore mt-5">
          <h5 class="singapore-text">City Guide: Singapore</h5>
        </div>
        <button type="button" class="btn btn-danger my-button">VIEW ALL CITY GUIDES</button>
        
      </aside>
    </div>
  </div>
</template>

<script>
import FarmCard from './FarmCard.vue'
import FoodCard from './FoodCard.vue'

export default {
  name: 'Farm',
  components:{
    FarmCard,
    FoodCard
  }
}
</script>

<style lang="scss">
.farm-cards{
  width: 68%;
  .loader{
    background-color: #EDEDE7;
    width: 100%;
    border: none;

  }
}
aside{
  width: 28%;
  .latest-recipes-box{
    position: relative;
    width: 100%;
    height: 430px;
    background-image: url("../assets/img/ad-bg.jpg");
    background-size: cover;
    
    .latest-recipes-text{
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 150px;

    }
  }
  .singapore{
    position: relative;
    width: 100%;
    height: 200px;
    background-image: url('../assets/img/singapore-featured-image.jpg');
    background-size: cover;
    .singapore-text{
      position: absolute;
      top: 60%;
      width: 230px;
      color: white;
      background-color: rgba(0, 0, 0, 0.781);
      padding: 10px;
    }
  }
  .my-button{
    width: 100%;
  }
  
}

</style>