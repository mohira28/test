<template>
  <div class="form">
    <form @submit="onSubmit">
        <label>Наименование товара</label> <br>
        <input v-model="name" type="text" id="name" placeholder="Введите наименование товара"/>

        <label>Описание товара</label> <br>
        <textarea v-model="description" placeholder="Введите описание товара"  rows="5"></textarea>

        <label>Ссылка на изображение товара</label> <br>
        <input v-model="url" type="url"  placeholder="Введите ссылку"/>

        <label>Цена товара</label> <br>
        <input v-model="price" type="number"  placeholder="Введите цену"/>

        <button :class="disabled">Добавить товар</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'FormComponent',

  data () {
    return {
      isfull: false,
      name: '',
      description: '',
      url: '',
      price: ''
    }
  },
  methods: {
    onSubmit (e) {
      e.preventDefault()
      const newProduct = {
        id: Math.random(),
        name: this.name,
        description: this.description,
        img: this.url,
        price: this.price
      }
      this.$emit('add-product', newProduct)
      console.log(newProduct)
      this.name = ''
      this.description = ''
      this.url = ''
      this.price = ''
    }
  }
}
</script>

<style scoped>
.form{
    font-family: 'Source Sans Pro';
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 13px;
    margin: 10px;
    width: 340px;
    height: auto;
    background-color: #fff;
    text-align: left;
    border-radius: 3px;
    padding: 5px;
    box-shadow: 1px 1px 4px rgb(216, 216, 216);
}
input, textarea, button{
  margin: 10px;
  width: 90%;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  border: none;
  outline: none;
}
input, button{
  height: 36px;
}
.notactive-btn{
  border: none;
  background-color: rgb(230, 230, 230);
  color: rgb(124, 124, 124);
}
.active-btn{
  border: none;
  background-color: green;
  color: white;
}
</style>
