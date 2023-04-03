<template>
  <div>
    <h1>Your Cart</h1>
    <div class="pieces">
      <div class="card">
        <div v-for="(piece, index) in cart" :key="index">
          <h3>{{ piece.name }}</h3>
          <h4>{{ piece.cost }}</h4>
          <img :src="piece.image" />
          <button v-on:click="removeItemFromCart">Remove</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["cart"],
  methods: {
    removeItemFromCart(piece) {
      this.$emit("removeItemFromCart", piece);
    },
  },
};
</script>

<style></style>
