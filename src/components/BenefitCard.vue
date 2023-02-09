<template>
  <div class="col-3 benefitcard d-flex flex-column align-items-center justify-content-evenly">
    <h5>{{ title }}</h5>
    <span class="m-3"><i :class="icon"></i></span>
    <div>
      <p>{{ benefit }}</p>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'BenefitCard',
    props: {
      title: String,
      icon: String,
      benefit: String
    }
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/BenefitCard.scss';
</style>