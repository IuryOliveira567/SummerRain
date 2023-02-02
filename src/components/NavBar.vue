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

<style scoped>
  .nav li a {
    color: #3B3E6D;
  }
  .nav li a:hover {
    opacity: 0.7;
    color: #3B3E6D;
  }

  .login, .signin {
    font-size: 0.8rem;
    padding: 8px 10px;
  }

  .login {
    background-color: #3B3E6D;
    color: white;
  }

  .signin {
    color: #3B3E6D;
    background-color: white;
    border: 1px solid #3B3E6D;
  }

  .mobile-menu {
    display: none;
    border: 1px solid #3B3E6D;
    border-radius: 3px;
    cursor: pointer;
  }
  .mobile-menu div {
    background-color: #3B3E6D;
    margin: 8px;
    width: 32px;
    height: 4px;
    border-radius: 4px;
  }

  @media(max-width: 988px) {
    .links, .logo {
      display: none;
    }
    .links {
      position: absolute;
      top: 8vh;
      left: 0;
      background-color: #3B3E6D;
      flex-direction: column;
      height: 90vh;
      width: 100vw;
      align-items: center;
      justify-content: space-around;
      z-index:  999;
    }

    .links li a {
      color: white;
    }

    .active {
      display: flex;
    }

    .mobile-menu {
      display: block;
    }

    .hide {
      display: none;
    }
    .rotate-left {
      transform: rotateZ(32deg) translateX(3px) translateY(5px);
    }
    .rotate-right {
      transform: rotateZ(-32deg) translateX(3px) translateY(-5px);
    }

    .rotate-left, .rotate-right {
      transition-duration: 0.3s;
    }
    .nav-bar {
      justify-content: space-between !important;
    }
    
  }
</style>      