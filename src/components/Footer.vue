<template>
  <footer>
    <Subscribe />
    
    <div class="images d-flex">
      <img 
      v-for="(image, index) in images"
      :key="index"
      :src="require(`../assets/img/${image}`)" alt="">
    </div>

    <Contacts :social='social'
    :menu='menu'/>
    <div class="copyright d-flex align-items-center justify-content-center">
      <p class="grey-text">
        <i class="far fa-copyright"></i>
        Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress
      </p>
      <i class="fas fa-chevron-circle-up my-chevron"></i>
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
  props:{
    social: Array,
    menu: Array
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
.copyright{
  position: relative;
  height: 80px;
  p{
    font-size: 0.7rem;
    margin-bottom: 0;
  }
  i{
    color: #464646;
    &.my-chevron{
      position: absolute;
      top: 5px;
      left: 50px;
      font-size: 2rem;
    }
    
  }
}
</style>