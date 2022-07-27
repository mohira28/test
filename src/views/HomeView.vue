<template>
  <ProductsComponent :products="products"/>
  <Form id="form" @add-product="addProduct"/>
</template>

<script>
import Form from '@/components/Form.vue'
import ProductsComponent from '@/components/Products.vue'

export default {
  name: 'HomeView',
  components: { ProductsComponent, Form },
  methods: {
    addProduct (product) {
      this.products = [...this.products, product]
    }
  },
  data () {
    return {
      products: [
        {
          id: 1,
          name: 'Наименование товара',
          description: 'Довольно таки интересное описание товара в несколько строк. Довольно таки интересное описание товара в несколько строк',
          img: 'https://instax.com/common2/img/camera/camera_01_04.png',
          price: 10000
        },
        {
          id: 2,
          name: 'Flowers',
          description: 'This flowers was made in China',
          img: 'https://news.cgtn.com/news/2020-09-20/Spider-flower-The-flower-with-a-distinctive-display-TVYLozFKg0/img/9c42156e261a4d2282370c03fce43a0a/9c42156e261a4d2282370c03fce43a0a.jpeg',
          price: 15000
        },
        {
          id: 3,
          name: 'laptop',
          description: 'This laptop was made in China',
          img: 'https://www.notebookcheck-ru.com/uploads/tx_nbc2/MicrosoftSurfaceLaptop3-15__1__02.JPG',
          price: 15000
        },
        {
          id: 4,
          name: 'cat',
          description: 'This cat was made in China',
          img: 'https://i.ytimg.com/vi/1Ne1hqOXKKI/maxresdefault.jpg',
          price: 15000
        }
      ]
    }
  }
}
</script>
<style scoped>
#form{
  position: absolute;
  top: 50px;
}
</style>
