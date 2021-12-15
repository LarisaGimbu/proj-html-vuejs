<template>
  <div class="culinary container pt-5">
    <div class="description text-center">
      <h3>CULINARY COLLECTION</h3>
      <p class="grey-text">Lorem ipsum dolor, sit amet consectetur adipisicing elit. <br/> Quam mollitia nam dignissimos facilis voluptatibus.</p>
    </div>
    <div class="culinary-cards d-flex flex-wrap justify-content-between pt-5">
      <div 
      v-for="(collection, index) in collections"
      :key="index"
      class="culinary-card text-center">
        <img :src="require(`../assets/img/${collection.image}`)" alt="">
        <p>{{collection.name}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Culinary',
  data(){
    return{
      collections:[
        {
          image: 'drinks-recipes.png',
          name: 'DRINKS'
        },
        {
          image: 'soups-recipes.png',
          name: 'SOUPS'
        },
        {
          image: 'baking-recipes.png',
          name: 'BAKERY'
        },
        {
          image: 'dinner-recipes.png',
          name: 'DINNER'
        },
        {
          image: 'healthy-recipes.png',
          name: 'HEALTHY'
        },
        {
          image: 'staff-picks.png',
          name: 'STAFF PICKS'
        },
        {
          image: 'premium-recipes.png',
          name: 'APPETISERS'
        },
        {
          image: 'quick-easy-recipes.png',
          name: 'QUICK & EASY'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';
@import '../assets/style/utilities.scss';

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
      p{
        line-height: 50px;
        width: 90%;
        margin: 0 auto;
      }
      &:hover p{
        background-color: $primary-color;
        cursor: pointer;
      }
    }
  }

</style>