<script setup>
import { ref } from 'vue';
//ref est comme une boite qui stock une valeur; actuellement on a mis 'Socks' dans cette boite, Vue garde un oeil sur lui(ref), 
// des que la valeur a l'interieur de ref change, tout ce qui est dans l'app et qui l'utlise se met a jour automatiquement

const product = ref('Boots')
</script>

<template>
  <div class="product-display">
    <div class="product-container">
      <div class="product-info">
        <h1>{{ product }}</h1>
      </div>
    </div>
  </div>
</template>