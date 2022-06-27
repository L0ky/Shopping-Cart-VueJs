<template>
  <header class="shadow-md relative">
    <nav class="flex justify-between px-10 lg:px-40 py-5 items-center">
      <div>
        <img src="/assets/logo.svg" width="50" alt="" />
      </div>
      <div class="lg:block hidden">
        <a href="#" class="text-lg">Accueil</a>
      </div>
      <div class="lg:block hidden">
        <a href="#" class="text-lg">Boutique</a>
      </div>
      <div
        v-on:click="isHidden = !isHidden"
        class="w-10 h-12 flex items-center relative cursor-pointer"
      >
        <i class="fa-solid fa-cart-shopping fa-xl"></i>
        <div
          class="absolute top-0 right-0 rounded-full w-5 h-5 bg-red-500 flex items-center justify-center"
        >
          <span class="text-white">{{ cart.length }}</span>
        </div>
      </div>
    </nav>
    <div v-if="isHidden" class="absolute right-1 top-24 w-80">
      <cart-pop-up />
    </div>
  </header>
</template>

<script>
import { useCart } from "../stores/useCart";
import CartPopUp from "./CartPopUp.vue";

export default {
  components: {
    CartPopUp,
  },
  setup() {
    return { cart: useCart() };
  },
  data() {
    return {
      isHidden: false,
    };
  },
};
</script>

<style></style>
