<template>
  <footer>
    <div class="container">
      <ul class="footer__links">
        <li><a href="" >Sobre</a></li>
        <li><a href="">Promoções</a></li>
      </ul>
      <ul class="footer__links_contact">
        <li><a href="" ><img src="../../public/iconLinkedin.svg" class="iconImage" alt="Logo do linkedin" title="Direciona para o Linkedin"></a></li>
        <li><a href=""><img src="../../public/iconInsta.svg" class="iconImage" alt="Logo do Instagram" title="Direciona para o Instagram"></a></li>
      </ul>
      <div class="footer__details">
        <p class="description-footer">Fotos: unsplash</p>
        <p class="description-footer">Desenvolvido por Angélica Shigematsu</p>
        <p class="description-footer"> &copy; 2023 - 2024 Todos os direitos reservados</p>
      </div>
    </div>
  </footer>
</template>

<style>

.iconImage {
  width: 120%;

}
footer {
  margin-top: 10vh;
  background-color: #1B1B1B;
  height: 40vh;
}

.footer__links_contact {
  display: flex;
  justify-content: flex-end;
}

.footer__details {
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  height: 10vh;
  text-align: center;
}

.footer__links {
  padding-top: 4%;
}
footer, .footer__links a {
  color: #ffffff;
}
</style>