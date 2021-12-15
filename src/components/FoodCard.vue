<template>
  <div class="my-card mt-2 mb-2">
      <img :src="require(`../assets/img/${image}`)" alt="">
      <div class="description text-cxenter">
        <h5 class="text-center pt-3">{{title}}</h5>
        <p class="text-center grey-text">{{date}} </p>
      </div>
    </div>
</template>

<script>
export default {
  name: 'FoodCard',
  props:{
    image: String,
    title: String,
    date: String
  }
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';

.my-card{
  background-color: white;
  width: 350px;
  img{
    width: 100%;
  }
  .description{
    border: none;
    width: 75%;
    margin: 0 auto;
  }
}

</style>