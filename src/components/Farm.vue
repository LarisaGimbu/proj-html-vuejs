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
        <div class="d-flex flex-wrap justify-content-between pt-5">
          <FoodCard v-for="(food, index) in foodies" :key="index" 
          :image="food.image"
          :title="food.title"
          :date="food.date" />
        </div>

        <button type="button" class=" loader btn btn-outline-dark mt-5">LOAD MORE POSTS</button>
      </div>  

      <FarmAside 
      :social='social'/>
      
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
  },
  props:{
    social: Array,
  },
  data(){
    return{
      foodies:[
        {
          image:'fi-roundup.jpg',
          title:'Roundup: My New Favourite Recipes For Healthy Living',
          date:'By admin | March 25th, 2019'
        },
        {
          image: 'fi-korean-food.jpg',
          title: 'Meal Prep: Korean Bibimbap with Kimchi',
          date: 'By admin | March 25th, 2019'
        },
        {
          image:'fi-toasts.jpg',
          title:'Why These Toasts with Tea are My New Favourite',
          date:'By admin | March 25th, 2019'
        },
        {
          image: 'fi-street-food.jpg',
          title: 'Exploring Street Food in Bankok',
          date: 'By admin | March 25th, 2019'
        },
        {
          image: 'fi-organic-breakfast.jpg',
          title: 'Organic Choices For Healthies Living',
          date: 'By admin | March 25th, 2019'
        },
        {
          image: 'fi-water-side-rest.jpg',
          title: '5 Waterside Restaurants in Istanbul for Special Events',
          date: 'By admin | March 25th, 2019'
        },
      ]
    }
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