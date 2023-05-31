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
        <ProductList
          v-for="(product, i) in inventory.slice(0, 3)" :key="product.id"
          :productDetails='product'
          :index=i
          :addToCart='addToCart'
         />
      </div>
      <div class="centered-div"><button class="big-btn btn-dark" @click="this.$router.push('/products')">View all items</button></div>
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
