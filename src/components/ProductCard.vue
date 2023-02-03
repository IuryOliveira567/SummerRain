<template>
  <div class="card rounded rounded-5">
    <slot></slot>
    <strong><span class="name">{{ name }}</span></strong>
    <span><strong class="price">${{ price }}</strong></span>
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

<style lang="scss" scoped>
  @import "../assets/scss/ProductCard.scss";
</style>