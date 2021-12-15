<template>
  <aside>
    <div class="latest-recipes-box">
      <h4 class="latest-recipes-text text-center">VIEW OUR LATEST RECIPES</h4>
    </div>

    <div class="singapore mt-5">
      <h5 class="singapore-text">City Guide: Singapore</h5>
    </div>
    <button type="button" class="btn btn-danger my-button">VIEW ALL CITY GUIDES</button>
        
    <div class="line pt-5"></div>
        
    <div class="input-group mb-3 pt-5">
      <button class="btn btn-outline-secondary search-btn" type="button" id="button-addon1"><i class="fas fa-search"></i></button>
      <input type="text" class="form-control search-input" placeholder="Search..." aria-label="Example text with button addon" aria-describedby="button-addon1">
    </div>

    <div class="social pt-5">
      <p>Follow Us</p>
      <p>SOCIAL</p>
    </div>

    <div class="guide">
      <div class="pb-2">
        <button class="btn btn-outline-secondary guide-btn active" type="button">Popular</button>
        <button class="btn btn-outline-secondary guide-btn" type="button">Recent</button>
      </div>

      <div class="guide-card d-flex pt-3">
        <div class="icon">
          <img class="guide-img" src="../assets/img/single-post-img3-66x66.jpg" alt="">
        </div>
        <div class="data">
          <p>Text</p>
          <p class="grey-text">Date</p>
        </div> 
      </div>

      <div class="tweet">TWEET</div>
    </div>
  </aside>
</template>

<script>
export default {
  name: 'FarmAside'
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';
@import '../assets/style/utilities.scss';

aside{
  width: 28%;
  .latest-recipes-box{
    position: relative;
    width: 100%;
    height: 430px;
    background-image: url("../assets/img/ad-bg.jpg");
    background-size: cover;
    
    .latest-recipes-text{
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 150px;

    }
  }
  .singapore{
    position: relative;
    width: 100%;
    height: 200px;
    background-image: url('../assets/img/singapore-featured-image.jpg');
    background-size: cover;
    .singapore-text{
      position: absolute;
      top: 60%;
      width: 230px;
      color: white;
      background-color: rgba(0, 0, 0, 0.781);
      padding: 10px;
    }
  }
  .my-button{
    width: 100%;
  }
  .line{
    width: 100%;
    border-bottom: 1px solid $light-grey;

  }
  .search-btn, .search-input{
    border: 2px solid $light-grey;
    color: #AAAAAA;
    background-color: white;
    padding-top: 15px;
    padding-bottom: 15px;
  }
  .search-btn{
    border-right: none;
  }
  .search-input{
    border-left: none;
  }
  .social p{
    color: $primary-color;
  }
  .guide{
    .guide-btn{
      width: 50%;
      border-radius: 0;
      padding: 15px 0 15px 0;
      border: 1px solid $light-grey;
      color: black;
      &.active{
        background-color: white;
        border-right: none;
      }
    }
    .guide-img{
      // width: 50px;
      // height: 50px;
      border-radius: 50%;
    }
  }
}
</style>