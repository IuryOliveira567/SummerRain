<template>
  <div>
    <div class="row mb-5">
      <header class="col-12 fixed-top bg-light">
        <NavBar/>
      </header>
    </div>
    <div class="row main">
      <main class="mt-5">
        <div class="main-pane d-flex justify-content-around">
          <div class="left-pane">
            <h1 class="fs-1">Get the Best<br>
            Products</h1>
            <h3 class="fs-4">From our Store</h3><br>
            <a class="getStartedBtn fs-5" href="#">Get Started<i class="fa fa-angle-right fa-align-right"></i></a>
          </div>
          <div class="right-pane d-flex align-items-start pt-4">
            <img class="img-pane rounded rounded-5 cursor-pointer" src="../src/assets/images/right-pane-image2.jpg" width="90%" height="80%" alt="Left Pane Image" />
          </div>
        </div>
      </main>
    </div>
    <div class="row products">
      <section class="mt-3">
        <h1>Products</h1>
        <div class="d-flex justify-content-around flex-wrap">
        <ProductCard
          v-for="(item, index) in products"
          :key="index"
          :name="item.name"
          :price="item.price"
          :stars="item.stars"
        >
        <img class="img-fluid rounded rounded-4" :src="item.cardImage" width="80%" height="40%" :alt="item.description"/>
        </ProductCard>
        </div>
      </section>
    </div>
    <div class="row benefit-section p-1 d-flex flex-row justify-content-around">
      <h1 class="fs-2 mt-4 mb-4">Optimizing your Business</h1>
      <BenefitCard
        v-for="(benefit, index) in benefitList" 
        :key="index"
        :title="benefit.title"
        :icon="benefit.icon"
        :benefit="benefit.description"
      />
    </div>
    <div class="row">
      <FooterPane/>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import { BootstrapVue, IconsPlugin } from 'bootstrap-vue'

import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

Vue.use(BootstrapVue)
Vue.use(IconsPlugin)

import NavBar from './components/NavBar.vue'
import ProductCard from './components/ProductCard.vue'
import FooterPane from './components/Footer.vue'
import BenefitCard from './components/BenefitCard.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    ProductCard,
    BenefitCard,
    FooterPane
  },
  data() {
    return {
      baseUrlCards: "../src/assets/images/product-images/",
      products: [
        {id: 0, name: 'Watch', description: 'Belt Watch', cardImage: require("../src/assets/images/product-images/watch.jpg"), price:19.81, stars: 5},
        {id: 1, name: 'Imac', description: 'iMac', cardImage: require("../src/assets/images/product-images/imac.jpg"), price: 1249.73, stars: 5},
        {id: 2, name: 'Iphone', description: 'Iphone', cardImage: require("../src/assets/images/product-images/iphone.png"), price: 699.99, stars: 4},
        {id: 3, name: 'Black Suit', description: 'Suit', cardImage: require("../src/assets/images/product-images/suit2.png"), price: 219.99, stars: 5},
        {id: 4, name: 'Kit mouse & keyboard', description: 'Kit mouse & keyboard', cardImage: require("../src/assets/images/product-images/peripherals.jpg"), price: 34.99, stars: 3},
        {id: 5, name: 'Sapphire ring', description: 'Sapphire ring', cardImage: require("../src/assets/images/product-images/sapphire-ring.jpg"), price: 1600.35, stars: 5},
        {id: 6, name: 'Tablet', description: 'tablet', cardImage: require("../src/assets/images/product-images/tablet.jpg"), price: 65.99, stars: 4},
        {id: 7, name: 'Sneakers', description: 'Sneakers', cardImage: require("../src/assets/images/product-images/sneakers.jpg"), price: 39.98, stars: 5},
        {id: 8, name: 'Play station 5 joystick', description: 'Play station 5 joystick', cardImage: require("../src/assets/images/product-images/joystick-playstation.jpg"), price: 69.45, stars: 4},
      ],
      benefitList: [
        {title: "Product comparison", icon: "fa fa-balance-scale", description: "Compare products to find exactly what<br> you are looking for"},
        {title: "Documents & drawings", icon: "fa fa-file-text-o", description: "Documents and drawings for your<br> convenience"},
        {title: "Select and configure", icon: "fa fa-wpforms", description: "With configurator tool one can<br> customize products with variety<br> options"},
        {title: "For logged in users", icon: "fa fa-wpforms", description: "For logged in users we offer the<br> posibility to view prices and check<br> availability"},
      ]
    }
  }
}
</script>

<style>

header {
  font-weight: 600;
}

main {
  height: auto;
}

.main-pane {
  height: 100%;
}

.left-pane {
  padding-left: 10%;
  padding-top: 7%;
}

.left-pane  * {
   margin: 1rem;
}

.left-pane h1, h3 {
  color: #3B3E6D;
}

.left-pane h1 {
  font-size: 3.2rem;
}

.right-pane img {
  cursor: pointer;
}

.getStartedBtn {
  background-color: #3B3E6D;
  color: white;
  text-decoration: none;
  padding: 8px 20px;
  border-radius: 5px;
}

.getStartedBtn:hover {
  color:#3B3E6D;
  background-color: white;
  border: 1px solid #3B3E6D;
  transition-duration: 0.3s;
}

.benefit-section {
  height: auto;
  background-color: #EBEBEB;
  color:#3B3E6D;
}

.products {
  height: 200%;
  margin-bottom: 3%;
}

.products h1 {
  color:#3B3E6D;
  margin-left: 5px;
}

.footer-pane {
  height: 60vh;
}

@media(max-width: 1125px) {
  body {
    font-size: 0.8rem;
  }

  .img-pane {
    height: 80%;
  }

  .left-pane {
    padding-left: 5%;
    width: 40vw;
  }

  .left-pane * {
    margin-top: 5%;
    padding-left: 5%;
  }
}

@media(max-width: 992px) {
   .products {
     height: 175vh;
     margin-top: 5%;
   }

   .main-pane {
     height: 50vh;
   }

   section {
    margin-top: 0;
   }

   .img-pane {
     height: 100%;
     width: 50vw;
   }
}

@media(max-width: 700px) {
  .left-pane {
    width: 40vw !important;
    padding-left: 0 !important;
  }

  .right-pane {
    width: 60vw !important;
  }
}

@media(max-width: 769px) {
  .products {
    height: auto;
    padding: 0;
  }

  .main-pane {
    display: flex;
  }

  .left-pane, .right-pane {
    width: 100vw;
    text-align: center;
  }

  .img-pane {
    display: block;
    margin: auto;
    width: 80%;
    height: 70%;
  }
}

@media(max-width: 682px) {
  .getStartedBtn {
    padding: 8px 8px;
  }

  .left-pane {
    padding-left: 2%;
    padding-top: 7%;
  }
}

@media(max-width: 578px) {
  .left-pane {
    width: 100vw !important;
  }

  .getStartedBtn i {
    display: none;
  }

  .right-pane {
    display: none !important;
  }
}

@media(max-width: 520px) {
  .benefit-section {
    height: auto;
  }
}

</style>
