<template>
  <main class="flex">
    <div id="app">
      <item-navegation></item-navegation>
      <container-products></container-products>
      <item-cart></item-cart>
      <login-item></login-item>
      <register-form></register-form>
  
    </div>
  </main>
</template>

<script>
import ItemNavegation from './components/ItemNavegation.vue'
import ContainerProducts from './components/ContainerProducts.vue'
import ItemCart from './components/ItemCart.vue'
import LoginItem from './components/forms/LoginForm.vue'
import RegisterForm from './components/forms/RegisterForm.vue'





export default {
  name: 'App',  
  components: {
    ItemNavegation,
    ContainerProducts,
    LoginItem,
    RegisterForm,
    ItemCart,
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
