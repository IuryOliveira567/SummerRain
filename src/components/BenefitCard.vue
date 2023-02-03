<template>
  <div class="col-3 benefitcard d-flex flex-column align-items-center">
    <h5>{{ title }}</h5>
    <span><i :class="icon"></i></span>
    <div class="d-flex align-items-center" v-html="benefit"></div>
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