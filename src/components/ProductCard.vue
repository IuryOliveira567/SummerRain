<template>
  <div class="card rounded rounded-5">
    <slot></slot>
    <strong><span class="text-md fs-5">{{ name }}</span></strong>
    <span><strong>${{ price }}</strong></span>
    <StarRating :stars="stars"/><br>
    <button class="buy-button">Buy now</button><br>
  </div>
</template>

<script>
  import StarRating from './StarRating.vue'

  export default {
    name: 'ProductCard',
    components: {
      StarRating
    },
    props: {
      name: String,
      price: Number,
      stars: Number
    }
  }
</script>

<style scoped>
  .card {
    width: 27%;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    padding: 5px;
    margin: 10px;
    cursor: pointer;
    box-shadow: 1px 1px 8px black;
  }

  .card:hover {
    transform: scale(1.01);
  }

  .card * {
    margin: 2px;
  }

  .buy-button {
    border-radius: 10px;
    padding: 6px;
    border: none;
  }

  .buy-button {
    color: white;
    background-color: #3A3E6D;
    width: 80%;
  }

</style>