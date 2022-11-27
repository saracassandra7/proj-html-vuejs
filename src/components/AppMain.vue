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

<div class="container-fluid colored">
  <div class="my-container">
    <div class="row">
    <AppSections/>
  </div>
  </div>
</div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/vars' as *;

.colored{
  background-color: $bg-colored;
  padding-bottom: 80px;
}

</style>