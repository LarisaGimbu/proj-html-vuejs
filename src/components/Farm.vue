<template>
  <div class="farm container pt-5 pb-5 d-flex justify-content-between">
    <div class="farm-content">
      <div class="description">
        <h3>FARM TO TABLE</h3>
        <p class="grey-text">Lorem ipsum dolor, sit amet consectetur adipisicing elit. <br/> Quam mollitia nam dignissimos facilis voluptatibus.</p>
      </div>
      <FarmCard />
      
      <div class="d-flex flex-wrap justify-content-between">
        <FoodCard v-for="card in 6" :key="card" />
      </div>

      <button type="button" class="btn btn-outline-dark">LOAD MORE POSTS</button>
    </div>

    <aside>
      <button type="button" class="btn btn-danger my-button">READ OUR BLOG</button>

    </aside>
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
.farm-content{
  width: 62%;
}

</style>