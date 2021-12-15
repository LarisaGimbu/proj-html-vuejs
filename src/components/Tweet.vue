<template>
  <div class="tweet">
    <div class="container pt-4">
      <div class="tweet-top d-flex justify-content-between align-items-center">
        <div class="title d-flex align-items-center">
          <h5 class="pe-2">Tweets</h5>
          <span>by <a href="#">@Theme_Fusion</a></span>
        </div>
        <i class="fas fa-info grey-text"></i>
      </div>
      <div class="pt-3 d-flex">
        <aside>
          <img src="../assets/img/3a74ce3d0532b7773b174c45ca3bd05a_normal.png" alt="">
        </aside>
        <div class="content">
          <div class="top-content d-flex justify-content-between">
            <div class="user">
              <h6>ThemeFusion</h6>
              <a href="#">@Theme_Fusion</a>
            </div>
            <div class="logo">
              <img src="../assets/img/image (1).svg" alt="">
            </div>
          </div>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto praesentium eligendi corrupti fugit est quod dolorum nemo deserunt asperiores ut provident sit, porro animi aliquam voluptatem, sequi unde dicta cupiditate?</p>
          <img src="../assets/img/En2TRxLW4AEiWUN.jpeg" alt="">
          <div class="d-flex bd-highlight mb-3 bottom-content ">
            <div class="p-2 bd-highlight">
              <i class="far fa-heart pe-3"></i>
            </div>
            <div class="p-2 bd-highlight">
              <i class="fas fa-sign-out-alt"></i>
            </div>
            <div class="ms-auto p-2 bd-highlight">
              <p class="align-self-end">21h</p>
            </div>
          </div>
          
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Tweet'
}
</script>

<style lang="scss">
@import '../assets/style/general.scss';
@import '../assets/style/vars.scss';
@import '../assets/style/utilities.scss';

.tweet{
  background-color: white;
  border-radius: 2%;
  .tweet-top{
    h5{
      margin-bottom: 0;
    }
    span{
      font-size: 0.8rem;
      a{
        color: #2B7BB9;
      }
    }
    i{
      height: 15px;
      border: 1px solid $grey-text;
      border-radius: 50%;
      font-size: 0.6rem;
      padding: 2px 5px 2px 5px;
    }
  }
  aside{
    width: 15%;
    height: 100%;
    img{
      width: 35px;
    }
  }
  .content{
    width: 85%;
    .user{
      font-size: 0.8rem;
      h6{
        margin-bottom: 0;
        font-weight: bold;
      }
      a{
        color: #657786;
      }
    }
    .logo img{
      width: 20px;
    }
    img{
      width: 100%;
      border-radius: 5%;
    }
    .bottom-content{
      i, p{
        color: $grey-text;
      }
    }
  }
}
</style>