<template>
  <div class="product">
    <main class="wrapper">
      <h1>Products</h1>

      <div class="card-container">
        <ProductList :inventory='inventory' :addToCart='addToCart'/>
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
