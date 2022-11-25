<script>
import {topNews, bottomNews} from '../assets/data/atricle'

export default {
  name: 'AppNews',

  data(){
    return{
      topNews,
      bottomNews
    }
  }

}
</script>

<template>
<h3 class="text-center">news</h3>

<div class="col-4" v-for="article in topNews" :key="article.id">
  <div class="article">
    <div class="img mb-3">
      <img :src="article.imgPath" :alt="article.alt">
    </div>
    <div class="text">
      <h6 class="fw-bold mb-1">{{article.title}}</h6>
      <span class="info">{{article.date}} | {{article.comments}}</span>
      <p class="description mt-2">{{article.description}}</p>
    </div>
  </div>

</div>

<div class="col-12">
  <div class="adv me-4">
    <div class="adv-content">
      <span class="text-uppercase fw-bold">featured article</span>
      <h3 class="fw-bold mt-3 mb-3">Cras malesuada et orci eget pharetra</h3>
      <p>Ipsum exercitationem nostrum possimus aperiam sed, quod repellat aliquid tenetur harum tempore rerum, debitis sit? Ipsam velit dolores odio placeat fugit ipsa.</p>
      <div class="my-btn">
       read more <i class="fa-solid fa-chevron-right"></i>
      </div>
    </div>  

  </div>
</div>

<div class="col-4" v-for="article in bottomNews" :key="article.id">
  <div class="article">
    <div class="img mb-3">
      <img :src="article.imgPath" :alt="article.alt">
    </div>
    <div class="text">
      <h6 class="fw-bold mb-1">{{article.title}}</h6>
      <span class="info">{{article.date}} | {{article.comments}}</span>
      <p class="description mt-2">{{article.description}}</p>
    </div>
  </div>

</div>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;

.article{

  .text{

    h6{
      font-size: 1.1rem;
    }

    .info, .description{
      color: grey;
    }

    .info{
      font-size: .8rem;
    }

    .description{
      font-size: .9rem;
      line-height: 160%;
    }
  }
};

.adv{
  height: 500px;
  background-image: url(../assets/images/featured_article_1_bg.jpg);
  background-position: center;
  background-size: cover;
  margin-top: 40px;
  margin-bottom: 60px;
  @include centerFlex('both');
  color: white;

  .adv-content{
    width: 80%;
    margin-top: 90px;

    span{
      font-size: .8rem;
      letter-spacing: .3rem;
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

</style>