<template>
  <header class="container">
    <div class="header-top d-flex justify-content-between align-intems-center">
      <ul>
        <li class="pe-3"><a href="#">Download App</a></li>
        <li><a href="#">Advertise with us</a></li>
      </ul>
      <ul>
        <li>SOCIAL</li>
      </ul>
    </div>
    <div class="logo d-flex justify-content-center">
      <img src="../assets/img/avada-food-logo.png" alt="">
    </div>

    <nav>NAVBAR</nav>
  </header>
</template>

<script>
export default {
  name:'Header'
}
</script>

<style lang="scss">
.header-top{
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
</style>
