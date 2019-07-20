<template>
  <div class="shopping">
    <h1>Shopping Cart Example</h1>
    <hr />
    <h2>Products</h2>
    <ProductList />
    <hr />
    <ShoppingCard />
  </div>
</template>

<script>
import ProductList from '../components/ProductList.vue'
import ShoppingCard from '../components/ShoppingCard.vue'

export default {
  components: {
    ProductList,
    ShoppingCard
  }

}
</script>
