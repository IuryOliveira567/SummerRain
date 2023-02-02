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

  @media(max-width: 940px) {
    .benefitcard {
      width: 50%;
      padding: 10px;
    }
  }

  @media(max-width: 561px) {
    .benefitcard {
      width: 100%;
      border-top: 1px solid lightgray;
    }
  }

</style>