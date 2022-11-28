<script>
export default {
  name:'AppFooterTop'

}
</script>

<template>
  <footer>
    <div class="top">
      <div class="content-top text-center">
        <h2 class="fw-bold">Hey! Join to our Community</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. At facilis expedita tenetur ut quia hic dolorum.</p>
        <div class="my-btn">
         sign up <i class="fa-solid fa-chevron-right"></i>
        </div>
      </div>
    </div>

    <div class="bottom">
      <div class="content-bottom">
        <h4 class="fw-bold text-center">Subscribe to our Newsletter</h4>
        <div class="input">
          <input type="text" placeholder="Insert your email*">
          <div class="my-btn">
            send
          </div>
        </div>
      </div>

    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/vars' as *;

footer{
  height: 800px;

  .top{
    height: 500px;
    background-image: url(../assets/images/join_now_cta_bg.jpg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    color: white;
    @include centerFlex('both');

    .content-top{
      width: 35%;

      h2{
        font-size: 3rem;
      }

      p{
        margin: 20px 0;
      }

      .my-btn{
        @include btnStyle();
        background-color: $eastern-blue;
        margin: 0 auto;
        width: 140px;
        text-align: center;
        font-size: 1rem;
      }

    }
  }

  .bottom{
    height: 300px;
    background-color: $bg-colored;
    color: black;
    @include centerFlex('both');

    .input{
      display: flex;
      margin: 30px 0;

      input{
        width: 30vw;
        height: 45px;
        border: 1px solid lightgray;
      }

      .my-btn{
        @include btnStyle();
        background-color: #191919;
        margin: 0 auto;
        width: 200px;
        text-align: center;
        font-size: .9rem;
        margin-left: 30px;
      }
    }
  }
}

</style>