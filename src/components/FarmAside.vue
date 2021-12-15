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
      <p class="follow-us">Follow Us</p>
      <ul>
        <li
        v-for="(item, index) in social" 
        :key="index"
        class="me-3"><a href="#"><i :class="`fab fa-${item}`"></i></a></li>
      </ul>
    </div>

    <div class="guide">
      <div class="pb-2">
        <button class="btn btn-outline-secondary guide-btn active" type="button">Popular</button>
        <button class="btn btn-outline-secondary guide-btn" type="button">Recent</button>
      </div>

      <div 
      v-for="(item, index) in populars"
      :key="index"
      class="guide-card d-flex pt-3">
        <div class="icon pe-3">
          <img class="guide-img" :src="require(`../assets/img/${item.image}`)" alt="">
        </div>
        <div class="text">
          <p>{{item.title}}</p>
          <p class="grey-text">{{item.date}}</p>
        </div> 
      </div>

      <Tweet />
    </div>
  </aside>
</template>

<script>
import Tweet from './Tweet.vue'

export default {
  name: 'FarmAside',
  components:{
    Tweet
  },
  props:{
    social: Array,
  },
  data(){
    return{
      populars:[
        {
          image: 'single-post-img3-66x66.jpg',
          title: 'Food Corner: Top Japanese Restaurants for Sushi',
          date:'March 25th, 2019'
        },
        {
          image: 'singapore-featured-image-66x66.jpg',
          title: 'City Guide: Singapore',
          date:'February 27th, 2019'
        },
        {
          image: 'slide1-bg-66x66.jpg',
          title: '6 Nutritional Tips to Help Burn Body Fat',
          date:'February 28th, 2019'
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
  .social{
    .follow-us{
      color: $primary-color;
    }
    ul{
      list-style: none;
      li{
        display: inline-block;
        background-color: #EDEDE8;
        border: 1px solid #E6E6E0;
        padding: 5px 10px 5px 10px;
        border-radius: 5px;
        a{
          text-decoration: none;
          font-size: 0.8rem;
          color: $grey-text;
        }
      }
    }
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
      width: 45px;
      height: 45px;
      border-radius: 50%;
    }
    p{
      font-size: 0.9rem;
      margin-bottom: 0.5rem;
    }
  }
}
</style>