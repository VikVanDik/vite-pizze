<script>
export default {

  name : 'CardPizza',

  props : {
    pizzaObj : Object
  },

  data (){
    return {

    }
  },

  computed : {
    ingredients (){
      return this.pizzaObj.ingredienti.join(', ')
    },

    price (){
      return `Prezzo : &euro; ${this.pizzaObj.prezzo.toFixed(2, '0')}`
    }
  }
  
}

</script>

<template>

  <div class="col my-3 ">
    <div class="card" style="width: 18rem;">
      <img :src="`/img/${pizzaObj.immagine}`" class="card-img-top" alt="">
      <div class="card-body">
        <h5 class="card-title">{{ pizzaObj.nome }}</h5>
        <p class="card-text">Ingredienti: {{ ingredients }}</p>
        <p class="card-text" v-html="price"></p>
      </div>
    </div>
  </div>
  
</template>

<style lang="scss">



</style>
