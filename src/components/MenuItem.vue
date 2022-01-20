<script>
export default {
  name: "MenuItem",
  props: ["addToShoppingCart", "image", "name", "inStock", "quantity"],
};
</script>

<template>
  <div class="menu-item">
    <img class="menu-item__image" :src="image.source" :alt="image.alt" />
    <div>
      <h3>{{ name }}</h3>
      <p v-if="inStock">En stock</p>
      <p v-else>En rupture de Stock</p>
      <div>
        <label for="add-item-quantity">Quantité : {{ amount }}</label>
        <input v-model.number="amount" id="add-item-quantity" type="number" />
        <button @click="addToShoppingCart(amount)">Ajouter au panier</button>
      </div>
    </div>
  </div>
</template>

<style></style>
