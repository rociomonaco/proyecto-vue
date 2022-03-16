<template>
  <tr class="p-5">
    <td>
      <div class="flex items-center justify-center">
        <div class="w-1/4 mr-3">
          <img src="@/assets/products/product-1.png" alt="" />
        </div>
        <div>
          <p>Spicy seasoned seafood noodles</p>
          <p>$ 2.29</p>
        </div>
      </div>
    </td>
    <td>
      <div class="flex flex-col items-center justify-center">
        <p>2</p>
      </div>
    </td>
    <td>
      <p>$ 2.29</p>
      <button><i class="fa-solid fa-trash-can"></i></button>
    </td>
  </tr>
</template>

<script>
export default {
    name: "ItemCart",
};
</script>

<style>
</style>