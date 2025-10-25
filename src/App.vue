<script setup>
import { ref } from 'vue'
import socksGreenImage from './assets/images/socks_green.jpeg'
import socksBlueImage from './assets/images/socks_blue.jpeg'

const product = ref('Socks')
const image = ref(socksGreenImage)
const inStock = true
  
const details = ref(['50% cotton', '30% wool', '20% polyester'])

const variants = ref([
  { id: 2234, color: 'green', image: socksGreenImage },
  { id: 2235, color: 'blue', image: socksBlueImage },
])

const cart = ref(0)

//On cree la fonction addToCard qui sera appelé sur button
const addToCard = () => cart.value += 1 //value correspond ref(0)

const updateImage = (variantImage) => { //variantImage correspond à variant.image qui est le paramettre de la fonction
  image.value = variantImage
}
</script>
  
<template>
  <div class="nav-bar"></div>
  <div class="cart">Cart({{ cart }})</div>
  <div class="product-display">
    <div class="product-container">
      <div class="product-image">    
        <img v-bind:src="image">
      </div>
      <div class="product-info">
        <h1>{{ product }}</h1>
        <p v-if="inStock">In Stock</p>
        <p v-else>Out of Stock</p>
        <ul>
          <li v-for="detail in details">{{ detail }}</li>
        </ul>
        <div
          v-for="variant in variants"
          :key="variant.id"
          @mouseover="updateImage(variant.image)"
        >
          {{ variant.color }}
        </div>
        <button class="button" @:click="addToCard">Add to Cart</button>
        <!-- <button class="button" v-on:click="addToCard">Add to Cart</button> -->
      </div>
    </div>
  </div>
</template>