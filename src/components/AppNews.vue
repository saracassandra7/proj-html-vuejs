<script>
import articles from '../assets/data/atricle'

export default {
  name: 'AppNews',

  data(){
    return{
      articles
    }
  }

}
</script>

<template>

<div class="col-4" v-for="article in articles" :key="article.id">
  <div class="article">
    <div class="img">
      <img :src="`./images/${article.imgPath}`" :alt="article.alt">
    </div>
    <div class="text">
      <h6 class="fw-bold">{{article.title}}</h6>
      <span class="info">{{article.date}} | <strong class="text-black">{{article.comments}}</strong> </span>
      <p class="description">{{article.description}}</p>
    </div>
  </div>

</div>

</template>

<style lang="scss" scoped>

.article{

  .text{

    .info, .description{
      color: grey;
      font-size: .9rem;
    }
  }
}

</style>