<template>
  <div class="nav-bar d-flex justify-content-between align-items-center p-1">
    <div class="mobile-menu" @click="showMenu">
      <div class="line1"></div>
      <div class="line2"></div>
      <div class="line3"></div>
    </div>
    <div class="img-logo">
      <a href="#"><img class="logo rounded rounded-2" src="../assets/images/logo.png" alt="mouse flow logo"/></a>
    </div>
    <nav>
      <ul class="nav links">
        <li class="nav-item"><a class="nav-link" href="#">PRICING</a></li>
        <li class="nav-item"><a class="nav-link" href="#">FEATURES</a></li>
        <li class="nav-item"><a class="nav-link" href="#">CLIENTS</a></li>
        <li class="nav-item"><a class="nav-link" href="#">TRAINING</a></li>
        <li class="nav-item"><a class="nav-link" href="#">CONTACTS</a></li>
        <li class="nav-item"><a class="nav-link" href="#">SUPPORT</a></li>
      </ul>
    </nav>
    <div class="d-flex justify-content-end">
      <a class="login rounded text-white nav-link m-1" href="#">LOG IN</a>
      <a class="signin rounded nav-link m-1" href="#">SIGN UP</a>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'NavBar',
    methods: {
      showMenu: function() {
        const mobileMenu = document.getElementsByClassName("nav")[0];
        mobileMenu.classList.toggle("active");

        const line1 = document.getElementsByClassName("line1")[0];
        line1.classList.toggle("hide");

        const line2 = document.getElementsByClassName("line2")[0];
        line2.classList.toggle("rotate-left");

        const line3 = document.getElementsByClassName("line3")[0];
        line3.classList.toggle("rotate-right");
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import "../assets/scss/NavBar.scss";
</style>