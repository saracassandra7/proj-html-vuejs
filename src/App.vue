<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
import menu from './assets/data/header-menu'

export default {
  name: 'App',

  data(){
    return{
      menu
    }
  },

  components:{
    AppHeader,
    AppMain,
    AppFooter,
  }
  
}
</script>

<template>
<AppHeader :menu="menu" />
<AppMain/>
<AppFooter/>
  
</template>

<style lang="scss">
@use './styles/general';

</style>