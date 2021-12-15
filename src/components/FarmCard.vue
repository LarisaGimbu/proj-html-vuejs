<template>
  <div class="farm-card">
    <div class="image">
      <img src="../assets/img/single-post-img3.jpg" alt="">
      <div class="text-hover justify-content-center align-items-center flex-column">
        <i class="fas fa-link"></i>
        <h5 class="text-center pt-3">Lunch Favourite with Salad, Naan And Beans</h5>
      </div>
    </div>
    
    <div class="farm-content">
      <h5>Food Corner: Top Japanese Restaurants for Sushi</h5>
      <p class="subtitle grey-text">Lorem ipsum dolor sit amet, consectetur</p>
      <div class="d-flex">
        <span class="points" v-for="punto in 120" :key="punto">.</span>
      </div>
      <p class="grey-text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ullam modi dicta, inventore eos quae rem eius veritatis quis suscipit autem eaque deserunt error ab cupiditate natus voluptates dolorum, minus saepe! </p>
      <a class="grey-text pt-5 pb-5" href="#">Read More ></a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FarmCard'
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';
@import '../assets/style/utilities.scss';

.farm-card{
  width: 100%;
  background-color: white;
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
      background-image: linear-gradient($background-primary-color, $primary-color);
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
  .farm-content{
    width: 90%;
    margin: 0 auto;
    padding: 30px 0 30px 0;
    a{
      text-decoration: none;
    }
  }
}
</style>