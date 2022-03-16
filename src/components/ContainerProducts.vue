<template>
        <section class="containerListProducts px-8 pt-5">
          <!-- header list product -->
          <div class="flex flex-row headerListProducts justify-between">
              <!-- 1er col -->
              <div>
                  <h1 class="text-5xl font-bold mb-4">Jaegar Resto</h1>
                  <p class="text-neutral-400">Tuesday, 2 Feb 2021</p>
              </div>
              <!--/ 1er col -->
              <!-- 2da col -->
              <div>
                  <div class="flex flex-row containerSearch p-2 rounded-lg">
                      <label class="px-1 cursor-pointer" for="tb_search"><img src="@/assets/icons/search.png" alt="search icon"></label>
                      <input class="tb_search" type="search" placeholder="Search for food, coffe, etc.." id="tb_search">
                  </div>
              </div>
              <!--/ 2da col -->
          </div>
          <!--/ header list product -->

          <!-- category -->
          <div class="categoryProducts mt-8 mb-8">
              <ul class="flex text-red-400 flex-row space-x-2.5 justify-start font-semibold">
                  <li class="cursor-pointer">Hot Dishes</li>
                  <li class="cursor-pointer">Cold Dishes</li>
                  <li class="cursor-pointer">Soup</li>
                  <li class="cursor-pointer">Grill</li>
                  <li class="cursor-pointer">Appetizer</li>
                  <li class="cursor-pointer">Dessert</li>
              </ul>
          </div>
          <!--/ category -->

          <!-- container food products -->
          <div>
              <h2 class="text-3xl my-3 font-semibold text-stone-50">Choose Dishes</h2>

              <!-- food products -->
              <div class="mt-24 w-full flex flex-row">
                <!--/ item -->
                 <item-product v-for="p in products" :key="p.index" :nombre="p.nombre" :imagen="p.imagen" :precio="p.precio" :stock="p.stock" :cantidad="p.cantidad" :seleccionado="p.seleccionado"></item-product>
                <!--/ item -->
                  
                  
              </div>
              <!--/ food products -->
          </div>
          <!--/ container food products -->

      </section>
</template>

<script>
import ItemProduct from './ItemProduct.vue'

export default {
  name: "ContainerProducts",
   components: {
    ItemProduct
    },
       
    data() {
    return {
      products: [
        {
          nombre: "Spicy seasoned seafood noodles",
          precio: 250,
          imagen: "assets/products/product-1.png",
          categoria: "",
          stock: 20,
          cantidad: 0,
          seleccion: false
        },
        {
          nombre: "Spicy seasoned seafood noodles",
          precio: 250,
          imagen: "assets/products/product-1.png",
          categoria: "",
          stock: 20,
          cantidad: 0,
          seleccion: false
        },
        {
          nombre: "Spicy seasoned seafood noodles",
          precio: 250,
          imagen: "assets/products/product-1.png",
          categoria: "",
          stock: 20,
          cantidad: 0,
          seleccion: false          
        },
      ],
    };
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
