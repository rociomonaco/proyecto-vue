<template>
  <!-- item -->
  <div
    class="
      w-2/5
      p-5
      item
      bg-slate-900
      rounded-lg
      text-stone-50
      mx-2
      cursor-pointer
    "
  >
    <!-- img -->
    <div class="relative w-full">
      <img class="absolute -top-20 left-8" src="" alt="product #1" />
    </div>
    <!--/ img -->

    <!-- text details -->
    <div class="mt-20 text-center">
      <h3 class="px-8 mb-2">Spicy seasoned seafood noodles</h3>
      <p class="my-2">$ 2.29</p>
      <p class="text-neutral-300 my-2">20 Bowls available</p>
    </div>
    <!--/ text details -->
  </div>
  <!--/ item -->
</template>

<script>
export default {
  name: "ItemProduct",
  props: {
    nombre: String,
    precio: Number,
    categoria: String,
    imagen: String,
    stock: Number,
    seleccionado: Boolean,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
