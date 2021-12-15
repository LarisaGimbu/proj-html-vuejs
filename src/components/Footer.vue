<template>
  <footer>
    <Subscribe />
    
    <div class="images d-flex">
      <img 
      v-for="(image, index) in images"
      :key="index"
      :src="require(`../assets/img/${image}`)" alt="">
    </div>

    <Contacts />
    <div>
      <p>Copyright</p>
    </div>
  </footer>
</template>

<script>
import Subscribe from './Subscribe.vue'
import Contacts from './Contacts.vue'

export default {
  name: 'Footer',
  components:{
    Subscribe,
    Contacts
  },
  data(){
    return{
      images:['Yogurt-Nan.jpg', 'Mixed-fruits.jpg', 'r-rachel-park-366508-unsplash-min.jpg', 'r-michelle-tsang-500721-unsplash-min.jpg']
    }
  }
}
</script>

<style lang="scss">
.images{
  width: 100%;
  img{
    width: calc(100% / 4);
  }
}
</style>