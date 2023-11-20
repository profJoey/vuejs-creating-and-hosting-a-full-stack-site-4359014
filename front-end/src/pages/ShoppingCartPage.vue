<template>
  <h1>Shopping</h1>
  <div v-if="cartItems.length > 0">
  <div class="product-container" v-for="product in cartItems" :key="product.id">
    <img class="product-image" :src="product.image" />
    <div class="details-wrap">
      <h3>{{ product.name }}</h3>
      <p>{{ product.price }}</p>
    </div>
    <button class="remove-button">Remove from cart</button>
  </div>
  <button class="checkout-button">Checkout</button>
  </div>
  <div v-if="cartItems.length === 0">
    You don't have any items in your cart
  </div>
</template>

<script>
import { cartItems } from "../temp-data";
export default {
  name: "ShoppingCartPage",
  data() {
    return {
      cartItems: [],
    };
  },
};
</script>
