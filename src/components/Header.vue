<template>
  <header>
    <div class="container">
      <div class="header-top d-flex justify-content-between align-intems-center">
        <ul >
          <li class="pe-3"><a href="#">Download App</a></li>
          <li><a href="#">Advertise with us</a></li>
        </ul>
        <ul>
          <li
          v-for="(item, index) in social" 
          :key="index"
          class="pe-3"><a href="#"><i :class="`fab fa-${item}`"></i></a></li>
        </ul>
      </div>
      <div class="logo d-flex justify-content-center">
        <img src="../assets/img/avada-food-logo.png" alt="">
      </div>

      <nav class="header-bottom d-flex justify-content-center">
        <ul>
          <li 
          v-for="item in menu"
          :key="item"
          class="pe-5 pt-3"><a href="#">{{item}}</a></li>
          <li><i class="fas fa-search"></i></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name:'Header',
  props:{
    social: Array,
    menu: Array
  }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';

header{
  background-color: white;
  .header-top{
    li, a{
      color: $grey-text;
    }
    
  }
}
.header-top, .header-bottom{
  ul{
    list-style: none;
    li{
      display: inline-block;
      a{
        text-decoration: none;
        font-size: 0.8rem;
      }
    }
      
  }
}
nav ul li{
  a{
    padding-bottom: 10px;
    color: $normaltext-color;
    &:hover{
      border-bottom: 2px solid $primary-color;
      color: $primary-color;
    }
  }
  i{
    font-size: 0.8rem;
    padding: 10px;
    &:hover{
      cursor: pointer;
      color: $primary-color;
    }
  }
}
</style>
