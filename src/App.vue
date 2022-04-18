<template>
  <div id="app">
    <div class="container mt-5">
      <h2 class="text-center mb-5">Carrinho de compra</h2>

      <cart :products="products"/>
    </div>
  </div>

</template>

<script>
import Cart from '@/components/cart/Cart.vue'
export default {
  data () {
    return {
      products: [
        {id: 1,  phone: 'iphone 12pro', color: 'spacegray', amount: 7000, qty: 1},
        {id: 2,  phone: 'iphone 11pro', color: 'gold share', amount: 6000, qty: 1},
        {id: 3,  phone: 'iphone 10pro', color: 'green', amount: 5000, qty: 1},
        {id: 4,  phone: 'iphone 9pro', color: 'gold', amount: 4000, qty: 1},
        {id: 5,  phone: 'galaxy s22', color: 'black', amount: 8000, qty: 1}
      ]
    }
  },
  name: 'App',
  components: {
    Cart
  },
  methods: {

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
