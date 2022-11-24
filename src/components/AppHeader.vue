<script>
export default {
  name: 'AppHeader'

}
</script>

<template>
  <header>
    <div class="my-container ">
      <div class="logo">
        <img src="/logo.png" alt="logo">
      </div>
      <div class="menu">MENU</div>
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
}
}


</style>