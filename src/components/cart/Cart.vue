<template>
  <div class="card shadow">
    <div v-for="product in products" :key="product.id">
      <product
        :product="product"
        @delete="deleteProduct"
      />

    </div>

    <hr>

    <div class="card-footer d-flex align-items-center justify-content-between">
      <a href="">
        Continuar comprando
      </a>

      <div>
        <small class="text-muted">Total:</small> <span class="fs-5">R$200.20</span>
      </div>
    </div>
  </div>
</template>
<script>
import Product from '@/components/cart/Product.vue'

export default {
  data () {
    return {}
  },
  props: {
    products: {
      type: Array,
      default: () => ([])
    }
  },
  components: {
    Product
  },
  methods: {
    deleteProduct (product) {
      this.$emit('delete', product)
    }
  }
}
</script>
<style>

</style>
