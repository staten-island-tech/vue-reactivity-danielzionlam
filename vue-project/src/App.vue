<template>
  <div>
    <header>
      <button v-on:click="navigateTo('pieces')">View Pieces</button>
      {{ cart.length }} in cart
      <button v-on:click="navigateTo('cart')">View Cart</button>
    </header>

    <div v-if="page === 'cart'">
      <Cart v-on:removeItemFromCart="removeItemFromCart" :cart="cart" />
    </div>

    <div v-if="page === 'pieces'">
      <Pieces v-on:addItemToCart="addItemToCart" />
    </div>
  </div>
</template>

<script>
import Pieces from "./components/Pieces.vue";
import Cart from "./components/Cart.vue";
export default {
  name: "App",
  data: () => {
    return {
      page: "pieces",
      cart: [],
    };
  },
  methods: {
    addItemToCart(piece) {
      this.cart.push(piece);
    },
    removeItemFromCart(piece) {
      this.cart.splice(this.cart.indexOf(piece));
    },
    navigateTo(page) {
      this.page = page;
    },
  },
  components: { Pieces, Cart },
};
</script>

<style>
body {
  margin: 0;
}
.pieces {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-evenly;
}
h1 {
  font-size: 8rem;
  background-color: red;
  text-align: center;
}
h3 {
  font-size: 5rem;
}
h4 {
  font-size: 3.5rem;
}
img {
  height: 35rem;
  width: 35rem;
}
.pieces button {
  padding: 1rem;
  background-color: lightgrey;
  color: black;
  outline: none;
  border: none;
  font-weight: 750;
  font-size: 3rem;
}
.pieces {
  border: black;
  padding: 1rem;
  border-radius: 1.5rem;
}
@import url("https://fonts.googleapis.com/css2?family=Bitter:wght@400;700&display=swap%22%22");
html,
body,
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-size: 62.5%;
  justify-content: center;
}
body {
  font-family: "Bitter", serif;
}
</style>

<style scoped>
header {
  height: 60px;
  background-color: #ddd;
  box-shadow: 2px 2px 5px #999;
  text-align: right;
  font-size: 30px;
  padding-top: 20px;
}

header button {
  padding: 1rem;
  background-color: black;
  color: #ddd;
  outline: none;
  border: none;
  font-weight: 750;
}
</style>
>
