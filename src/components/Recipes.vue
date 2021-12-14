<template>
  <div class="recipes container pt-5">
    <div class="title text-center">
      <h5>POPULAR RECIPES</h5>
      <p class="description">Lorem ipsum dolor, sit amet consectetur adipisicing elit.<br/> Quam mollitia nam dignissimos facilis voluptatibus.</p>
    </div>
    <div class="content d-flex justify-content-between pt-5">
      <PopularCard />
      <h3>IMAGES</h3>
    </div>

  </div>
</template>

<script>
import PopularCard from './PopularCard.vue'

export default {
  name: 'Recipes',
  components:{
    PopularCard
  }
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';

.recipes{
  margin-top: 360px;
  .description{
    color: $grey-text;
  }
}

</style>