<script>
import AppJumbotron from './AppJumbotron.vue'
import AppNews from './AppNews.vue'

export default {
  name: 'AppMain',

  components:{
    AppJumbotron,
    AppNews
  }

}
</script>

<template>
<AppJumbotron/>
<!-- <div class="my-container">
  <div class="row">
    <AppNews/>
  </div>
</div> -->
</template>

<style lang="scss" scoped>

</style>