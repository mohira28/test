<template>
  <nav>
    <h4>Добавление товара</h4>
  </nav>
  <router-view/>
</template>
<script>
export default {
  components: {}
}
</script>

<style>
body{
  margin: 0;
  background-color: #E5E5E5;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #E5E5E5;
  color: black;
  padding: 30px 10px 0 10px;
}

nav a {
  font-size: 30px;
  text-decoration: none;
  font-weight: bold;
}

nav a.router-link-exact-active {
  color: #42b983;
}

</style>
