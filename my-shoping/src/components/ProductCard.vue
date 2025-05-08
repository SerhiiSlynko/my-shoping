<template>
  <div class="product-card">
    <img 
      class="product-image" 
      :src="image" 
      :alt="name" 
    />
    <h2>{{ name }}</h2>
    <p>{{ description }}</p>
    <p class="price">{{ price }} грн</p>
    <button class="buy-button">Купити</button>
  </div>
</template>

<script>
export default {
  name: 'ProductCard',
  props: {
    image: String,
    name: String,
    description: String,
    price: Number
  }
}
</script>

<style>
.product-card {
  border: 1px solid #ccc;
  border-radius: 8px;
  padding: 16px;
  text-align: center;
  width: 250px;
  margin: 20px auto;
}
.product-image {
  width: 100%;
  height: auto;
}
.price {
  font-weight: bold;
}
.buy-button {
  background-color: #42b983;
  color: white;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  border-radius: 4px;
}
.buy-button:hover {
  background-color: #369870;
}
</style>
