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
  <div class="row">
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
  
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;

.my-container{
  .col-3{
    h6{
      text-transform: uppercase;
      font-weight: bold;
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
            font-size: .8rem;

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

</style>