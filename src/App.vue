<template>
  <div>
    <Header 
    :social='social'
    :menu='menu'/>
    <Main 
    :social='social'/>
    <Footer 
    :social='social'
    :menu='menu'/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  },
  data(){
    return{
      social:['facebook-f', 'instagram', 'twitter', 'youtube'],
      menu:[
        {
          name: 'Home',
          active: true,
          id: 1234
        },
        {
          name: 'Recipes',
          active: false,
          id: 2345
        },
        {
          name: 'Places',
          active: false,
          id: 3456
        },
        {
          name: 'Blog',
          active: false,
          id: 4567
        },
        {
          name: 'About',
          active: false,
          id: 5678
        },
        {
          name: 'Contact',
          active: false,
          id: 6789
        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/general.scss';
@import './assets/style/vars.scss';

</style>
