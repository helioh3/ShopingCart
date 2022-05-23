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
        <small class="text-muted">Total:</small> <span class="fs-5">{{ total }}</span>
      </div>
    </div>
  </div>
</template>
<script>
import Product from '@/components/cart/Product.vue'

export default {
  props: {
    products: {
      type: Array,
      default: () => ([])
    }
  },
  computed: {
    total() {
      return this.products.reduce((getVal, item) => {
        getVal += item.qty * item.amount
        return getVal
      }, 0)
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
