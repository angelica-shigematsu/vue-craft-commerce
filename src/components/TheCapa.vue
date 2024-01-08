<template>
  <div class="header-backColor"></div>
  <div class="body-backColor"></div>
  <div class="container">
    <div class="front">
      <div class="text">
        <div class="title">Encontre Artesanato <br> <scan class="titleBold">Personalizado</scan></div>
        <div class="subtilte">Quadros de pinturas, bordados, arigurumi, crochê e entre outros</div>
      </div>
      <div >
        <img src="../assets/capa.jpg" alt="foto de dois coelhos feito de croche" class="imgRight">
      </div>
    </div>
  </div>
</template>

<script>

</script>

<style>
  .body-backColor {
    background: linear-gradient(90deg,  #dbb582,#D6AF78); 
    padding-top: 7vh;
    height: 600px;
    width: 100%;
    position: absolute;
  }
  .header-backColor {
    background-color: gold;
    padding-top: 7vh;
  }
 .front {
    position: relative;
    background-color: #dbb582;
    padding-top: 7vh;
    height: 600px;
  }
  .imgRight {
    width: 70%;
    float: right;
  }

  .subtitle {
    line-height: 60px;
  }

  .text {
    position: absolute;
    padding-top: 20vh;
    width: 38%;
    height: 30%;
  }
  .title {
    font-size: 2.4em;
    line-height: 45px;
  }

  .titleBold {
    font-weight: bold;
    color: gold;
    -webkit-text-stroke-width: 1px;
    text-shadow: black 1px 0 10px;
    letter-spacing: 3px;
  }
</style>