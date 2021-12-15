<template>
  <div class="contacts pt-5 pb-5">
    <div class="container d-flex justify-content-between">
      <div class="logo pe-5">
        <img src="../assets/img/avada-food-logo-mob-2x-200x87.png" alt="">
        <ul class="pt-4">
          <li
          v-for="(item, index) in social" 
          :key="index"
          class="pe-3 d-inline-block"><a href="#"><i :class="`fab fa-${item}`"></i></a></li>
        </ul>
      </div>
    
      <div class="pe-5">
        
        <ul>
          <li 
          v-for="item in menu"
          :key="item"
          class="pt-2 nav-bar"><a href="#">{{item}}</a></li>
        </ul>
      
      </div>
      <div class="pe-5 contact-content">
        <h6>CONTACT</h6>
        <ul>
          <li 
          class="pt-3"
          v-for="(contact, index) in contacts"
          :key="index">
            <i :class="`fas ${contact.fontawesome} pe-3`"></i>
            <span>{{contact.text}} </span>
          </li>
        </ul>
      </div>
      <div class="download d-flex flex-column">
        <h6>GET OUR APP!</h6>
        <img class="pt-4" src="../assets/img/download-android.png" alt="">
        <img class="pt-3" src="../assets/img/download-app-store.png" alt="">
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Contacts',
  props:{
    social: Array,
    menu: Array
  },
  data(){
    return{
      contacts:[
        {
          fontawesome: 'fa-map-marker-alt',
          text: '775 New York Ave, Brooklyn, Kings, New York 11203'
        },
        {
          fontawesome: 'fa-phone',
          text: ' 0100-505-0000'
        },
        {
          fontawesome: 'fa-envelope',
          text: 'info@your-domain.com'
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


.contacts{
  background-color: white;
  h6{
    color: $primary-color;
  }
  ul{
    list-style: none;
    padding-left: 0;
    li{
      a, i, span{
        text-decoration: none;
        font-size: 0.8rem;
        color: $grey-text;
      }
      .nav-bar{
        color: $normaltext-color;
      }
    }    
  }
  .contact-content{
    width: 250px;
  }
  .download{
    img{
      width: 200px;
    }
  }
  
}
</style>