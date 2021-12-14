<template>
  <div class="my-card mt-2 mb-2">
      <img src="../assets/img/single-post-img3-1200x790.jpg" alt="">
      <div class="description text-cxenter">
        <h4 class="text-center">Lorem ipsum dolor sit amet consectetur adipisicing</h4>
        <p class="text-center">Data</p>
      </div>
    </div>
</template>

<script>
export default {
  name: 'FoodCard'
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