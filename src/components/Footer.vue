<template>
    <div class="footer">
      <div>
        <h3>Product</h3>
        <ul>
          <li><a href="#">Tour</a></li>
          <li><a href="#">Pricing</a></li>
          <li><a href="#">News</a></li>
          <li><a href="#">Police Privacy</a></li>
          <li><a href="#">Term of Services</a></li>
        </ul>
      </div>
      <div>
        <h3>Social</h3>
        <ul>
          <li><a href="#">Facebook</a></li>
          <li><a href="#">Twitter</a></li>
          <li><a href="#">Instagram</a></li>
          <li><a href="#">Linkedin</a></li>
          <li><a href="#"></a></li>
        </ul>
      </div>
      <div>
        <h3>Help</h3>
        <ul>
          <li><a href="#">Customer Services</a></li>
          <li><a href="#">Delivery Options</a></li>
          <li><a href="#">Terms & Conditions</a></li>
          <li><a href="#">Privacy Notice</a></li>
          <li><a href="#"></a></li>
        </ul>
      </div>
      <div>
        <h3>Company</h3>
        <ul>
          <li><a href="#">About</a></li>
          <li><a href="#">Contacts</a></li>
          <li><a href="#">Support</a></li>
          <li><a href="#">FAQ</a></li>
          <li><a href="#">Careers</a></li>
        </ul>
      </div>
    </div>
</template>

<script>
  export default {
    name: 'FooterPane'
  }
</script>

<style scoped>
  .footer {
    background-color: #3B3E6D;
    height: 55vh;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
  }

  h3 {
    color: white;
    margin-bottom: 2rem;
  }
  .footer div {
    width: 20%;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    height: 80%;
    padding-left: 2%;
  }
  .footer div ul {
    list-style: none;
    padding: 0; 
  }
  .footer div ul li a {
    color: white;
    text-decoration: none;
    display: flex;
    padding-bottom: 1.2rem;
    justify-content: start;
  }
  .footer div ul li a:hover {
    opacity: 0.7;
  }

  @media(max-width: 730px) {
    .footer {
      flex-direction: column;
      height: 200vh;
    }

    .footer div {
      align-items: center;  
      width: 100vw;
    }

    div h3 {
      font-size: 2.3rem;
    }

    div ul li a {
      font-size: 1.1rem;
    }
  }
</style>