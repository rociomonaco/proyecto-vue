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
      <img class="absolute -top-20 left-8" :src="require('@/'+imagen + '')" alt="product #1" />
    </div>
    <!--/ img -->

    <!-- text details -->
    <div class="mt-20 text-center">
      <h3 class="px-8 mb-2">{{nombre}}</h3>
      <p class="my-2">$ {{precio}}</p>
      <p class="text-neutral-300 my-2">{{stock}} Bowls available</p>
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
.containerListProducts{
    width: 60%;
}
.headerListProducts, .categoryProducts{
    width: 100%;
    color: #fff;
}
.containerSearch{
    background-color: #2d303e;
}
.tb_search{
    background-color: transparent;
    outline: none;
}

.containerCart{
    width: 35%;
}


</style>
