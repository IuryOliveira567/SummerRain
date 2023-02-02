<template>
  <div class="card rounded rounded-5">
    <slot></slot>
    <strong><span class="name">{{ name }}</span></strong>
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
    box-shadow: 1px 1px 3px black;
  }

  .card:hover {
    transform: scale(1.01);
  }

  .card * {
    margin: 2px;
  }

  .name {
    font-size: 1.2rem;
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

  @media(max-width: 858px) {
    .card {
      width: 30%;
      height: 20%;
    }

    .name {
      font-size: 1rem;
    }
  }

  @media(max-width: 769px) {
    .card {
     width: 40%;
    }
  }

  @media(max-width: 520px) {
    .card {
      width: 45%;
    }

    .name {
      font-size: 0.9rem;
    }
  }


  @media(max-width: 400px) {
    .card {
      width: 60%;
    }
  }
</style>