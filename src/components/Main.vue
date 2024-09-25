<script>
import ProductCard from './partials/ProductCard.vue';
import productsList from '../assets/data/db.json';

  export default {

    components: {
      ProductCard
    },
    
    data(){
      return {
        productsList
      }
    }
  }

</script>



<template>

  <main>
    <div class="container">

      <ProductCard 
      v-for=" product in productsList.products"
      :key="product.id" 
      :product="product"/>

    </div>
    
  </main>

</template>




<style lang="scss" scoped>
@use '../assets/scss/partials/general';
@use '../assets/scss/partials/variables' as *;



.container {
	display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}
</style>