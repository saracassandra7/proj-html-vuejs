<script>
import AppJumbotron from './AppJumbotron.vue'
import AppNews from './AppNews.vue'
import AppTutorials from './AppTutorials.vue'
import AppSections from './AppSections.vue'

export default {
  name: 'AppMain',

  components:{
    AppJumbotron,
    AppNews,
    AppTutorials,
    AppSections
  }

}
</script>

<template>
<AppJumbotron/>

<div class="my-container">
  <div class="row">
    <AppNews/>
  </div>

  <div class="row">
    <AppTutorials/>
  </div>
  
</div>

<div class="black-stripe">
  <p>read our blog 
    <i class="fa-solid fa-arrow-right"></i>
  </p>
</div>

<div class="container-fluid colored">
  <div class="my-container">
    <div class="row">
    <AppSections/>
  </div>
  </div>
</div>

<div class="black-stripe">
  <p>go to our forum 
    <i class="fa-solid fa-arrow-right"></i>
  </p>
</div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/vars' as *;
@use '../styles/partials/mixin' as *;

.colored{
  background-color: $bg-colored;
  padding-bottom: 80px;
}

.black-stripe{
  @include blackStripe()
}

</style>