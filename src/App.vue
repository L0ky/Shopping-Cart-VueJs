<script setup>
import ProductList from "./components/ProductList.vue";
import HeaderCart from "./components/HeaderCart.vue";
</script>

<template>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css"
    integrity="sha512-KfkfwYDsLkIlwQp6LFnl8zNdLGxu9YAA1QvwINks4PhcElQSvqcyVLLD9aMhXd13uQjoXtEKNosOWaZqXgel0g=="
    crossorigin="anonymous"
    referrerpolicy="no-referrer"
  />
  <div class="sticky top-0 bg-white">
    <header-cart />
  </div>
  <div class="mt-20">
    <product-list />
  </div>
</template>

<style></style>
