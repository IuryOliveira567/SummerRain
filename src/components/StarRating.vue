<template>
  <div>
    <div class="d-inline">
    <span v-for="n in stars" :key="n" class="fa fa-star checked"></span>
    </div>
    <div class="d-inline">
    <span v-for="k in (5 - stars)" :key="k" class="fa fa-star"></span>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'StarRating',
    data() {
      return {
        starNumber: this.stars
      }
    },
    props: {
      stars: Number
    },
    computed: {
      starClass: function() {
        return this.starNumber? 'fa fa-star checked': 'fa-fa-stars'
      }
    }
  }
</script>

<style scoped>
  .checked {
    color: orange;
  }
</style>