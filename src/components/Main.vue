<script>
import products from '../data/products'
import Card from './Card.vue';

export default {
  name: 'Main',
  components: {
    Card
  },

  data() {
    return {
      products
    }
  },
}

</script>

<template>

<main>
  <div class="container-sm">
    <div class="cards">

      <Card 
        v-for="product in products"
        :key="product.id"
        :firstImage="product.imageMain" 
        :secondImage="product.imageAltern" 
        :discount="product.discount" 
        :eco="product.eco" 
        :brand="product.brand" 
        :type="product.type" 
        :firstPrice="product.price" 
        :lastPrice="product.priceDisc" 
      />
    
    </div>
  </div>
</main>

</template>

<style lang="scss" scoped>

.cards {
  margin: 50px 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 25px;
}

</style>
