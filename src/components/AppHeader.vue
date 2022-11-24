<script>
import menu from '../assets/data/header-menu'

export default {
  name: 'AppHeader',

  data(){
    return{
      menu
    }
  }

}
</script>

<template>
  <header>
    <div class="my-container ">
      <div class="logo">
        <img src="/logo.png" alt="logo">
      </div>
      <div class="menu d-flex align-items-center">
        <nav class="pt-3">
          <ul>
            <li class="text-capitalize" v-for="(link, index) in menu" :key="index">
              <a class="text-white" href="#">{{link.text}}</a>
            </li>
          </ul>
        </nav>

        <div class="my-btn ms-3 me-4">join us</div>
        <div class="search ms-2">
          <i class="fa-solid fa-magnifying-glass text-white"></i>
        </div>
      </div>
    </div>


  </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/vars' as *;


header{
  height: 80px;
  background-color: $eastern-blue;

  .my-container{
  @include centerFlex('vertical');
  justify-content: space-between;
  height: 100%;

  .logo img{
    width: 220px;
  }

  .menu{
    @include menuBasic();

    
    ul{
     @include centerFlex('vertical');
    
    }

    .my-btn{
      background-color: black;
      @include btnStyle();
      &:hover{
        background-color: rgba($color: #000000, $alpha: .8);
      }

    }

    i{
      cursor: pointer;
    }

    
  }
}
}


</style>