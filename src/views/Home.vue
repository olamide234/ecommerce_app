<template>
  <div class="home">
    <div class="splash-container">
      <div class="splash">
        <h1>Splendid Food</h1>
      </div>
    </div>

    <main class="wrapper">
      <h2>Recommended</h2>

      <div class="recommended">
        <ProductList :inventory='inventory.slice(0, 3)' :addToCart='addToCart'/>
      </div>
    </main>
  </div>
</template>

<script>
import ProductList from '../components/ProductList.vue'

export default {
  name: 'Home',
  props: ['inventory', 'addToCart'],
  components: { ProductList }
}
</script>
