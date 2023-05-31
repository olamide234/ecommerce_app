<template>
  <div class="product">
    <main class="wrapper">
      <h1>Products</h1>

      <div class="card-container">
        <ProductList
          v-for="(product, i) in inventory"
          :key="product.id"
          :productDetails='product'
          :index=i
          :addToCart='addToCart'
        />
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
