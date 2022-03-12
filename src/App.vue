<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <ItemProduct/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ItemProduct from './components/ItemProduct.vue'


export default {
  name: 'App',  
  data (){
    return {
      products: [
      {
        nombre: "Spicy seasoned seafood noodles",
        precio: 250,
        imagen: "./assets/products/product-1.png",
        categoria: "",
        stock: 20 
      },
      {
        nombre: "Spicy seasoned seafood noodles",
        precio: 250,
        imagen: "./assets/products/product-1.png",
        categoria: "",
        stock: 20 
      },
      {
        nombre: "Spicy seasoned seafood noodles",
        precio: 250,
        imagen: "./assets/products/product-1.png",
        categoria: "",
        stock: 20 
      }
    ]
    }
  },
  
  components: {
    HelloWorld,
    ItemProduct
  },

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
