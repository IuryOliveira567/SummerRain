<template>
  <div class="col-3 bnf">
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

<style scoped>
  .bnf {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    padding: 2px;
  }

  .bnf div {
    text-align: justify;
  }

  .bnf span i {
    font-size: 2rem;
  }
</style>