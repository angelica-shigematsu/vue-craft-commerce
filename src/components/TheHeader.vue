<template>
  <div class="container">
  <header class="header">
    <div class="logo">
    ARTEShop
    </div>
    <div>
      <ul class="menu">
        <li><a href="">PROMOÇÃO</a></li>

        <li><a href="">SOBRE</a></li>

        <li class="dropdown">
          <img src="./icons/notificationOff.png" 
            alt="notificacao"
          >
          <div 
            v-if="notification.quant"
            class="notification"
            >
            {{ notification.quant }}
          </div>
          
          <div class="dropdown-content"
            v-for="item in notification.product"
            :key="item.id">
            <p> {{ item.name }}</p>
          </div>
        </li>

        <li class="dropdown">
          <img src="./icons/cart.png" 
            alt="carrinho">
          <div 
            v-if="cart.quant"
            class="notification"
            >
            {{ cart.quant }}
          </div>

          <div class="dropdown-content"
            v-if="cart.quant">
            <li 
              v-for="item in cart.product"
            :key="item.id">
            <div
              v-if="item.quant">
              <p> {{ item.name }}</p> 
              <div class="card-quant">
                <p
                  @click="removeProduct(item.id)"
                  class="iconDiscreaseProduct">-</p>
                  <p>{{ cart.product[item.id-1].quant }}</p>
                <p
                  @click="addProduct(item.id)"
                  class="iconDiscreaseProduct">+</p>
                </div>
              </div>
            <hr>
            </li>
          </div>
        </li>
      </ul>
    </div>
  </header>
</div>
</template>

<script>
export default {
  data() {
    return{
      notification: {
        quant: 1,
        product: [{
          id: 3,
          name: "Bolsa de Crochê",
          quant: 1,
          price: 70.00
        }]
      },
      cart: {
        quant: 3,
        product: [{
          id: 1,
          name: "Vestido de Crochê",
          quant: 1,
          price: 30.00
        },
        {
          id: 2,
          name: "Sapato de crochê",
          quant: 2,
          price: 15.00
        },
      ]
      }
    }
  },
  methods: {
    addProduct(id) {
      this.cart.product.map(product=> product.id == id ? product.quant++: product.quant)
      this.cart.quant++
      return
    },
    removeProduct(id) {

      //less one product
      let quantProduct = this.cart.product.map(product=> product.id == id? product.quant--: product.quant)

      let product = this.cart.product.map(product=> product.id == id)

      let positionProduct = product.indexOf() + 1

      //update quantity of product in the cart
      this.cart.quant--;

      let hasZeroProduct = quantProduct == 0 && quantProduct != undefined

      if(hasZeroProduct) {
        //remove product in the cart (front-end)
        this.cart.product.splice(positionProduct, 1)
      }

      return 
    }
  }
}
</script>

<style>
  header {
    background-color: gold;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #000;
    height: 7vh;
    position: absolute;
    width: 1000px;
  }
  .menu {
    display: flex;
    flex-direction: row;
  }

  li {
    font-weight: 500;
    padding-right: 2vw;
  }

  .logo {
    font-size: 1.5em;
    font-weight: bold;
  }
  img {
    width: 50%;
  }

  .notification {
    background-color: #E3735E;
    border-radius: 50%;
    color: #fff;
    float: right;
    font-size: 0.8em;
    font-weight: bold;
    width: 40%;
    text-align: center;
  }

  scan {
    color:#E3735E;
  }

  /* cada card da lista do dropdown do carrinho */

  .iconDiscreaseProduct {
    border-radius: 50%;
    background-color: #E3735E;
    color: #fff;
    text-align: center;

  }

  .card-quant {
    display: flex;
    flex-direction: row;
    margin-bottom: 10%;
  }

  .card-quant p {
    padding: 0 2vw 0 2vw;
  }

  hr {
    height: 0.5px;
    border-width:0;
    background-color: gray;
  }


  /**************************************************************/

  /**********dropdown menu ***********/
.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  padding: 12px 16px;
  z-index: 1;
}

.dropdown:hover .dropdown-content {
  display: block;
}

.dropdown-content:hover +  {
  background-color: #E3735E;
  float: right;
}
</style>