<template>
  <main class="flex">
    <div id="app">
      <item-navegation></item-navegation>
      <container-products></container-products>
      <login-item></login-item>
    </div>
  </main>
</template>

<script>
import ItemNavegation from './components/ItemNavegation.vue'
import ContainerProducts from './components/ContainerProducts.vue'
import LoginItem from './components/login/LoginItem.vue'



export default {
  name: 'App',  
  components: {
    ItemNavegation,
    ContainerProducts,
    LoginItem
  },
 

}
</script>

<style>
*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

body{
    height: 100vh;
}
</style>
