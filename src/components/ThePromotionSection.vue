<template>
  <section class="container">
    <p class="sectionName">Promoções</p>
  <div class="sectionPromotion">
    <div class="product">
      <img src="../assets/crochet.jpg" alt="camiseta de crochê">
      <div class="description"><p class="nameProduct">Xale de Crochê</p><p class="priceUnit">R$50,00</p></div>
      <button class="buttonAdd" @click="isClicked()">Adicione no carrinho</button>
    </div>
    <div class="product">
      <img src="../assets/bag.jpg" alt="bolsa de macrame">
      <div class="description"><p class="nameProduct">Bolsa de macramê</p><p class="priceUnit">R$67,00</p></div>
      <button class="buttonAdd"  @click="isClicked()">Adicione no carrinho</button>
    </div>
    <div class="product">
      <img src="../assets/crochet.jpg" alt="camiseta de crochê">
      <div class="description"><p class="nameProduct">Xale de Crochê</p><p class="priceUnit">R$50,00</p></div>
      <button class="buttonAdd" @click="isClicked()">Adicione no carrinho</button>
    </div>
    </div>
  </section>  
</template>

<script>
export default {
 
}
</script>

<style>

.buttonAdd {
  background-color: gold;
  font-size: 1em;
  width: 55%;
  padding: 2% 4% 2% 4%;
  border: 1px solid gold;
}

.buttonAdd:hover {
  background-color: #fff;
  border:  1px solid black;
}

.description {
  display: flex;
  flex-direction: row;
}

.priceUnit {
  margin-left: 3%;
}

.product {
  padding-top: 6%;
  width: 35%;
  height: 60%;
  align-items: center;
  justify-content: center;
}

img {
  width: 55%;
  height: 60%;
}

.sectionPromotion {
  display: flex;
  flex-direction: row;
}
.sectionName {
  font-size: 1.2em;
}

</style>