<template>
  <div class="recipes container pt-5">
    <div class="title text-center">
      <h5>POPULAR RECIPES</h5>
      <p class="grey-text">Lorem ipsum dolor, sit amet consectetur adipisicing elit.<br/> Quam mollitia nam dignissimos facilis voluptatibus.</p>
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
  aside{
    width: 48%;
    .image-box{
      width: 47%;
    }
    .aside-images{
      width: 100%;
    }
  }
}

</style>