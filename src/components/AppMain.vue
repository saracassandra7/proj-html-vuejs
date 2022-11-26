<script>
import AppJumbotron from './AppJumbotron.vue'
import AppNews from './AppNews.vue'
import AppSections from './AppSections.vue'

export default {
  name: 'AppMain',

  components:{
    AppJumbotron,
    AppNews,
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

.colored{
  background-color: #f2f2f2;
}

</style>