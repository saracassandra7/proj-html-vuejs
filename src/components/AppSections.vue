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
  <div class="my-card me-4">
    <div class="icon">
      <i :class="card.icon"></i>
    </div>
    <span class="fw-bold">{{card.text}}</span>

  </div>
</div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;

.my-card{
  height: 170px;
  background-color: white;
  margin-bottom: 30px;
  border-top: 3px solid #9cdae3;
  @include centerFlex('both');
  flex-direction: column;

  .icon{
    height: 50px;
    width: 50px;
    background-color: #ff8d61;
    border-radius: 50%;
    @include centerFlex('both');
    margin-bottom: 15px;

    i{
      color: white;
      font-size: 1.3rem;
    }
  }

  span{
    font-size: 1.1rem;

  }
  
}

</style>