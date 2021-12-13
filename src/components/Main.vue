<template>
  <main>
    <Jumbotron />
    <Recipes />
    <h5>CULINARY COLLECTION</h5>
    <h5>FARM TO TABLE</h5>
  </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue'
import Recipes from './Recipes.vue'

export default {
  name: 'Main',
  components:{
    Jumbotron,
    Recipes
  }
}
</script>

<style lang="scss">

</style>