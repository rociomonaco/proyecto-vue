<template>
  <main id="app">
    <div class="flex">
      <item-navegation></item-navegation>
      <container-products></container-products>
      <container-cart></container-cart>
    </div>
    <login-form></login-form>
    <register-form></register-form>

  </main>
</template>

<script>
import ItemNavegation from './components/ItemNavegation.vue'
import ContainerProducts from './components/ContainerProducts.vue'
import ContainerCart from './components/ContainerCart.vue'

import LoginForm from './components/forms/LoginForm.vue'
import RegisterForm from './components/forms/RegisterForm.vue'





export default {
  name: 'App',  
  components: {
    ItemNavegation,
    ContainerProducts,
    LoginForm,
    RegisterForm,
    ContainerCart,
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
