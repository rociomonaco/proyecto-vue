<template>
 <!-- order -->
      <section class="containerCart flex justify-end">

          <!-- <div class="bg-red-400 mt-5 cursor-pointer px-4 w-20 h-20 rounded-br-lg rounded-tl-lg flex justify-center items-center">
              <i class="fa-solid fa-shrimp text-5xl"></i>
          </div>  -->

          <!-- open order -->
          <div class="containerCart_order bg-slate-900 max-h-screen w-full pt-4">
              <!-- headerCart_order -->
              <div>
                  <h2 class="text-stone-50">Orders #34562</h2>

                  <!-- where -->
                  <div class="my-5">
                      <ul class="text-stone-50 flex">
                          <li class="p-2 mx-2 bg-red-400 rounded-lg cursor-pointer">Dine in</li>
                          <li class="p-2 mx-2 text-red-400 border border-stone-50 rounded-lg cursor-pointer">To Go</li>
                          <li class="p-2 mx-2 text-red-400 border border-stone-50 rounded-lg cursor-pointer">Delivery</li>
                      </ul>
                  </div>
                  <!-- where -->
              </div>
              <!--/ headerCart_order -->

              <!-- container order -->
              <table class="table-auto text-neutral-300 bg-primary w-5/6  mx-auto">
                  <thead>
                    <tr>
                      <th>Item</th>
                      <th>Qty</th>
                      <th>Price</th>
                    </tr>
                  </thead>
                  <tbody>
                    <!-- Item Cart -->
                        <item-cart></item-cart>
                    <!-- Item Cart -->
                  </tbody>
                </table>
                <!--/ container order -->

          </div>
          <!--/ open order -->
      </section>
      <!--/ order -->
</template>

<script>
import ItemCart from './ItemCart.vue'

export default {
  name: "ContainerCart",
  components: {
    ItemCart
  },
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header, section{
    height: 100vh;
}
header{
    width: 5%;
}

nav ul{
    width: 100%;
    font-size: 1.8rem;
}
.nav-item{
    position: relative;
}
.nav-item:hover li:after, .nav-item:active li:after{
    content: "";
    width: 2rem;
    height: 2.65rem;
    background-color:  #393C49;
    position: absolute;
}
.nav-item:hover li, .nav-item:active li{
    background-color:  #393C49;
    border-radius: 8px 8px 8px 8px;
}

</style>
