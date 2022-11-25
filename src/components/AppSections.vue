<script>
import cards from '../assets/data/cards'
export default {
  name:'AppSections',

  data(){
    return{
      cards
    }
  }

}
</script>

<template>
<h3 class="text-center">Forum Sections</h3>

<div v-for="(card, index) in cards" :key="index" class="col-3">
  <div class="my-card">
    <div class="icon">
      <i :class="card.icon"></i>
    </div>
    <span>{{card.text}}</span>

  </div>
</div>
</template>

<style lang="scss" scoped>
.my-card{
  background-color: aqua;
  margin-bottom: 30px;
  text-align: center;
  border-top: 2px solid green;
  
}

</style>