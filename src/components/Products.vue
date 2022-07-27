<template>
  <div class="products">
    <div v-for="product in products" :key="product.id" id="grid">
        <ProductComponent :product="product"/>
    </div>
  </div>
</template>

<script>
import ProductComponent from './Product.vue'

export default {
  name: 'ProductsComponent',
  components: { ProductComponent },
  props: {
    products: Array
  }
}
</script>

<style>
*{
    margin: 0;
    padding: 0;
}
.products{
    margin: 0;
    margin-left: 360px;
    display: grid;
    grid-template-columns: auto auto auto;
}
#grid{
    text-align: center;
}
</style>
