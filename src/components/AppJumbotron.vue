<script>
export default {
  name: 'AppJumbotron'

}
</script>

<template>
<div class="jumbo">
  <div class="jumbotron">
  <div class="my-container">

    <div class="jumbo-content">
      <h1 class="mt-5">Tech Forum!</h1>
       <span>Discuss all the latest technology news and trends</span>
      <div class="my-btn">
       get avada now! <i class="fa-solid fa-chevron-right"></i>
      </div>

    </div>
  </div>

  <div class="jumbo-container">
    <div class="row justify-content-center">
      <div class="col-8 text-center">
        <span class="text-uppercase">avada forum is the place to be</span>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. <br>Velit dolor modi voluptate amet tempora voluptatem culpa maxime. <br>Laudantium eos distinctio eius laborum sit amet consectetur.</p>
      </div>
    </div>
  </div>

</div>
</div>

  
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/vars' as *;

.jumbo{
  height: 900px;

  .jumbotron{
  height: 600px;
  background-image: url(../assets/images/home_slider_bg.jpg);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  color: white;

  .my-container{
    height: 100%;

    .jumbo-content{
      @include centerFlex('horizontal');
      flex-direction: column;
      height: 100%;
      width: 100%;

      h1{
        font-size: 8rem;
        color: white;
        font-weight: 900;
      }

      span{
        font-size: 1.5rem;
      }

      .my-btn{
        @include btnStyle();
        background-color: $eastern-blue;
        margin: 30px 0;
        width: 210px;
        text-align: center;
        font-size: 1rem;
      }
    }
  };

  .jumbo-container{
    background-color: $bg-colored;
    height: 300px;
    
    color: grey;
    @include centerFlex('vertical');

    .row{
      width: 100%;
    }

    span{
      letter-spacing: .3rem;
      font-size: .8rem;
      font-weight: bold;
      color: rgb(78, 78, 78)
    };

    p{
      margin-top: 20px;
      line-height: 160%;
      font-size: 1.6rem;
      letter-spacing: .11rem;
    }
  }
}
}


</style>