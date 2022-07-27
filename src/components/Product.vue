<template>
  <div class="product">
    <img :src="product.img" alt="Product"/>
    <div class="desc">
        <h3>{{ product.name }}</h3>
        <p>{{ product.description }}</p>
        <h3>{{ product.price }} руб.</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductComponent',
  props: {
    product: Object
  }
}
</script>

<style>
.product{
    margin: 10px;
    height: auto;
    width: 280px;
    text-align: left;
    background-color: #fff;
    box-shadow: 1px 1px 4px rgb(216, 216, 216);
    transition: all 0.3s;
    text-align: left;
}
.product:hover{
    margin: 8px;
    height: auto;
    background-color: #fff;
    box-shadow: 3px 3px 10px rgb(115, 115, 115);
}
.product img{
    width: 100%;
    height: 30vh;
    border-radius: 3px 3px 0 0;
}
.product .desc{
    padding: 0 10px 30px 10px;
}
p{
    margin: 10px 0 10px;
}
</style>
