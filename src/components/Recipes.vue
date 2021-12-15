<template>
  <div class="recipes container pt-5">
    <div class="title d-flex flex-column justify-content-center align-items-center">
      <h5>POPULAR RECIPES</h5>
      <p class="grey-text recipes-text text-center">Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia loboris.</p>
    </div>
    <div class="content d-flex justify-content-between pt-5">
      <PopularCard />
      <aside class="d-flex flex-wrap justify-content-between">
        <div v-for="(image, index) in images" :key="index" class="image-box">
          <img class="aside-images" :src="require(`../assets/img/${image}`)" alt="">
        </div>
      </aside>
    </div>

  </div>
</template>

<script>
import PopularCard from './PopularCard.vue'

export default {
  name: 'Recipes',
  components:{
    PopularCard
  },
  data(){
    return{
      images:['Mixed-fruits.jpg', 'r-rachel-park-366508-unsplash-min.jpg', 'r-michelle-tsang-500721-unsplash-min.jpg', 'quick-summer-drink-460x295.jpg', 'r-maarten-van-den-heuvel-400626-unsplash-min-460x295.jpg', 'perfect-cosmopolitan-460x295.jpg', 'fi2x-6-460x295.jpg', 'r-brooke-lark-96398-unsplash-min-460x295.jpg']
    }
  }
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';

.recipes{
  margin-top: 360px;
  .recipes-text{
    width: 50%;
  }
  aside{
    width: 48%;
    .image-box{
      position: relative;
      width: 47%;
      .aside-images{
        width: 100%;
      }
    }
    
  }
}

</style>