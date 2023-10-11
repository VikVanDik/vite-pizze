<script>

import pizze from './data/pizze'
import CardPizza from './components/CardPizza.vue';

export default {
  name : 'App',


  data (){
    return {
      pizze
    }
  },

  components : {
    CardPizza
  },

  created (){
    console.log(this.pizze);
  }

}

</script>

<template>


  <div class="container my-5 ">
    <div class="row">
      <CardPizza v-for = "(pizza, index) in pizze" :key = "index" :pizzaObj="pizza"/>
      
    </div>
  </div>
  
</template>

<style lang="scss">

@import 'bootstrap/scss/bootstrap';

</style>
