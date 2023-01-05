<template>
  <div class="nav-bar d-flex justify-content-between align-items-center p-1">
    <div class="mobile-menu" @click="showMenu">
      <div></div>
      <div></div>
      <div></div>
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
      <a class="login p-2 rounded text-white nav-link m-1" href="#">LOG IN</a>
      <a class="signin p-2 rounded nav-link m-1" href="#">SIGN UP</a>
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
    font-size: 0.9rem;
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
      height: 80vh;
      width: 100vw;
      align-items: center;
      justify-content: space-around;
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

    .nav-bar {
      justify-content: space-between !important;
    }
    
  }
</style>      