<script>
import {tutorials} from '../assets/data/atricle'

export default {
  name:'AppTutorials',

  data(){
    return{
      tutorials
    }
  }

}
</script>

<template>
  <div class="container">
    <div class="row">
      
      <div class="col-8">
        <div class="review">
          <div class="content">
            <span class="text-uppercase fw-bold">reviewed product</span>
          <h2 class="fw-bold mt-3 mb-3">Lorem ipsum dolor sit amet consectetur adipisicing elit possimus aperiam</h2>
          <p>Ipsum exercitationem nostrum possimus aperiam sed, quod repellat aliquid tenetur harum tempore rerum, debitis sit? </p>
          <div class="my-btn">
           read more <i class="fa-solid fa-chevron-right"></i>
          </div>
          </div>
        </div>
      </div>

      <div class="col-4">
        <div class="title">
          <h4 class="fw-bold">Tutorials &amp; Guides </h4>
        </div>

        <div class="products">
          <div v-for="product in tutorials" :key="product.id" class="product d-flex mb-3">
            <div class="img">
              <img :src="product.imgPath" :alt="product.alt">
            </div>
            <div class="text">
              <h6 class="fw-bold">{{product.title}}</h6>
              <span>{{product.date}} | {{product.comments}}</span>
            </div>

          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;

.container{
  margin-top: 40px;
  margin-bottom: 60px;

  .row{
   width: 100%;

     .review{
        height: 400px;
        background-image: url(../assets/images/featured_article_2_bg.jpg);
        background-position: center;
        background-size: cover;
        @include centerFlex('both');
        color: white;

        .content{
          width: 85%;
          margin-top: 30px;

          span{
           font-size: .7rem;
           letter-spacing: .3rem;
          }

          p{
           font-size: .9rem;
          }

          .my-btn{
            @include btnStyle();
            background-color: black;
            margin: 30px 0;
            width: 140px;
            text-align: center;
          }
        }

      } 

    .title{
      position: relative;
      margin-bottom: 65px;
      h4::after{
       position: absolute;
       content: "";
       height: 2px;
       background-color: #f7c8b6;
       width: 65px;
       margin-left: 15px;
       top: 55px;
       left: -10px;


      }
    }  

    .product{
      
     .img{
      margin-right: 15px;

        img{
         width: 145px;

        }
    
      }

      span{
        font-size: .68rem;
        color: grey;
      }


    }


  }    


}
</style>