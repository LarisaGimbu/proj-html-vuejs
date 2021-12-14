<template>
  <div class="jumbotron d-flex justify-content-center align-items-center flex-column">
    
    <div class="todays-pick p-4 text-center">
      <div class="box-label p-2">TODAY'S PICK</div>
      <h1>Lorem ipsum dolor sit amet consectetur.</h1>
      <p class="date">March 25, 2019</p>
    </div>
    <div class="container foodies">
      <div class="foodie-title d-flex justify-content-center align-items-center">
        <span class="points" v-for="punto in 120" :key="punto">.</span>
        <h5 class="ps-5 pe-5">FOODIE JOURNAL</h5>
        <span class="points" v-for="punto in 120" :key="punto">.</span>
      </div>
      <FoodCard />
    </div>
  </div>
</template>

<script>
import FoodCard from './FoodCard.vue'

export default {
  name: 'Jumbotron',
  components:{
    FoodCard
  },
  data(){
    return{
      foodImg:['single-post-img3-1200x790.jpg', ],
      foodTitle:['Lorem'],
      foodDate:['2019']
    }
  }
  
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';
@import '../assets/style/utilities.scss';

.jumbotron{
  position: relative;
  width: 100%;
  min-height: 80vh;
  background-image: url("../assets/img/single-post-img3.jpg");
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
  }
  .foodies{
    position: absolute;
    bottom: -330px;
    padding: 20px 0 20px 0;
    background-color: white;
  }
}

</style>