<template>
  <ul>
    <li v-for="product in products" :key="product.id">
      {{ product.title }} - {{ product.price | currency }}
      <br />
      <v-btn :disabled="!product.inventory" @click="addProductToCart(product)">Add to cart</v-btn>
    </li>
  </ul>
</template>

<script>
import { mapState, mapActions } from 'vuex'

export default {
  computed: mapState({
    products: state => state.products.all
  }),
  methods: mapActions('cart', ['addProductToCart']),
  created () {
    this.$store.dispatch('products/getAllProducts')
  }
}
</script>
