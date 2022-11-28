<script>
import {popularTopics, recentTopics, latestReplies} from '../assets/data/footer-menu'

export default {
  name:'AppFooterBottom',

  data(){
    return{
      popularTopics,
      recentTopics,
      latestReplies
    }
  }

}
</script>

<template>
<div class="my-container mt-5">
  <div class="row mb-5">
    <div class="col-3">
      <h6>avada tech forum</h6>
      <p>Hic repellat eius, id odit quisquam atque ipsam consectetur blanditiis pariatur recusandae accusantium natus suscipit ipsa rerum reprehenderit.</p>
    </div>

    <div class="col-3">
      <h6>popular topics</h6>
      <nav>
        <ul>
          <li v-for="(link, index) in popularTopics" :key="index" >
            <i class="fa-solid fa-chevron-right"></i>
            <a :href="link.href">{{link.text}}</a>
          </li>
        </ul>
      </nav>
    </div>

    <div class="col-3">
      <h6>recent topics</h6>
      <nav>
        <ul>
          <li v-for="(link, index) in recentTopics" :key="index" >
            <i class="fa-solid fa-chevron-right"></i>
            <a :href="link.href">{{link.text}}</a>
          </li>
        </ul>
      </nav>
    </div>

    <div class="col-3">
      <h6>latest replies</h6>
      <nav>
        <ul>
          <li v-for="(link, index) in latestReplies" :key="index" >
            <i class="fa-solid fa-chevron-right"></i>
            <a :href="link.href">{{link.text}}</a>
          </li>
        </ul>
      </nav>
    </div>


  </div>
</div>

<div class="socials">
  <div class="my-container mt-4 mb-4 d-flex justify-content-between align-items-center">
    <div class="credits">
      &copy; Copyright 2012 - 2020 | Avada Theme by <strong>Theme Fusion</strong> | All Rights Reserved | Powered by <strong>WordPress</strong>
    </div>

    <div class="icons d-flex">
      <i class="fa-brands fa-facebook-f"></i>
      <i class="fa-brands fa-twitter"></i>
      <i class="fa-brands fa-instagram"></i>
      <i class="fa-brands fa-youtube"></i>
    </div>

  </div>
  <a href="#"><i class="fa-solid fa-chevron-up"></i></a>
</div>
  
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;

.my-container{
  .col-3{
    h6{
      text-transform: uppercase;
      font-weight: 900;
      font-size: .9rem;
    }

    p{
      font-size: .9rem;
      color: grey;
      padding-top: 10px
    }

    nav{
      @include menuBasic();
      
      ul{
        padding: 0;

        li{
          padding: 10px 0;
          border-bottom:  1px solid rgb(224, 224, 224);
          height: 70px;

          i{
            padding-right: 5px;
            font-size: .7rem;

          }

          a{
            color: black;
            font-size: .9rem;
            
          }

        }
      }
    }
  }
}

.socials{
  border-top: 1px solid rgb(224, 224, 224);
  position: relative;

  .credits{
    color: grey;
    font-size: .75rem;

    strong{
      color: black
    }
  }

  .icons i{
    height: 40px;
    width: 40px;
    border-radius: 50%;
    @include centerFlex('both');
    margin-bottom: 15px;
    color: white;
    margin-left: 10px;
    font-size: .9rem;
    cursor: pointer;
  }
  i:first-child{
    background-color: #3c5998;
  }
  i:nth-child(2){
    background-color: #54acee;
  }
  i:nth-child(3){
    background-color: #3f729b;
  }
  i:last-child{
    background-color: #cd201f;
  }

  i.fa-chevron-up{
    height: 35px;
    width: 40px;
    background-color: #474747;
    color: white;
    @include centerFlex('both');
    font-size: .8rem;
    position: absolute;
    right: 2%;
    top: 68px;
    border-top-left-radius: 4px;
    border-top-right-radius: 4px;
    cursor: pointer;
  }
}

</style>