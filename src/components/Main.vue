<template>
  <main>
    <Jumbotron />
    <Recipes />
    <Culinary />
    <Farm 
    :social='social'/>
  </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue'
import Recipes from './Recipes.vue'
import Culinary from './Culinary.vue'
import Farm from './Farm.vue'

export default {
  name: 'Main',
  components:{
    Jumbotron,
    Recipes,
    Culinary,
    Farm
  },
  props:{
    social: Array,
  },
  data(){
    return{
      
    }
  }
}
</script>

<style lang="scss">

</style>