<template>
  <div class="card">
    <div class="card-title">{{ productDetails.name }}</div>
    <div class="card-body">
      <i class="icofont-10x icofont-{{productDetails.icon}}"></i>
      <form>
        <div class="row">
          <div class="cell">
            <label>Type:</label>
          </div>
          <div class="cell">
            <em>{{ productDetails.type }}</em>
          </div>
        </div>
        <div class="row">
          <div class="cell">
            <label>Price:</label>
          </div>
          <div class="cell">${{ productDetails.price.USD }}</div>
        </div>
        <div class="row">
          <div class="cell">
            <label>Quantity:</label>
          </div>
          <div class="cell">
            <input type="number" v-model.number="quantity" />
          </div>
        </div>
      </form>
    </div>
    <div class="card-footer">
      <button @click="cartAddition(productDetails.name, quantity)" class="btn btn-light">
        Add to cart
      </button>
    </div>
  </div>
</template>

<script>

export default {
  props: ['productDetails', 'addToCart'],
  data () {
    return {
      quantity: 0
    }
  },
  methods: {
    cartAddition (name, quantity) {
      this.addToCart(name, quantity)
      this.quantity = 0
    }
  }
}
</script>
