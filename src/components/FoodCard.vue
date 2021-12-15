<template>
  <div class="my-card mt-2 mb-2">
    <div class="image">
      <img :src="require(`../assets/img/${image}`)" alt="">
      <div class="text-hover justify-content-center align-items-center flex-column">
        <i class="fas fa-link"></i>
        <h5 class="text-center pt-3">{{title}}</h5>
      </div>
    </div>
      
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
  .image{
    position: relative;
    img{
      width: 100%;
    }
    .text-hover{
      display: none;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 100%;
      height: 100%;
      color: white;
      background-image: linear-gradient($light-primary-color, $primary-color);
      i{
        background-color: white;
        padding: 10px;
        font-size: 1.5rem;
        color: $primary-color;
        border-radius: 50%;
        &:hover{
          transform: scale(1.3);
        }
      }
    }
    &:hover .text-hover{
      display: flex;
      cursor: pointer;
    }
  }
  .description{
    border: none;
    width: 75%;
    margin: 0 auto;
  }
}

</style>