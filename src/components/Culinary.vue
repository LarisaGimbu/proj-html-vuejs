<template>
  <div class="culinary container pt-5">
    <div class="description text-center">
      <h3>CULINARY COLLECTION</h3>
      <p class="grey-text">Lorem ipsum dolor, sit amet consectetur adipisicing elit. <br/> Quam mollitia nam dignissimos facilis voluptatibus.</p>
    </div>
    <div class="culinary-cards d-flex flex-wrap justify-content-between pt-5">
      <div 
      v-for="card in 8"
      :key="card"
      class="culinary-card text-center">
        <img src="../assets/img/drinks-recipes.png" alt="">
        <p>DRINKS</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Culinary'
}
</script>

<style lang="scss">
  .culinary-cards{
    width: 100%;
    .culinary-card{
      width: 22%;
      background-color: white;
      padding: 10px 0 10px 0;
      margin-bottom: 25px;
      img{
        width: 40%;
      }
    }
  }

</style>