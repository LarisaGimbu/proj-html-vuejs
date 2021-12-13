<template>
  <main>
    <Jumbotron />
    <Recipes />
    <Culinary />
    <h5>FARM TO TABLE</h5>
  </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue'
import Recipes from './Recipes.vue'
import Culinary from './Culinary.vue'

export default {
  name: 'Main',
  components:{
    Jumbotron,
    Recipes,
    Culinary
  }
}
</script>

<style lang="scss">

</style>