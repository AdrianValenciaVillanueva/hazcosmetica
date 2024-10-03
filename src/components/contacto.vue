<template>
  <div class="footer-section">
    <div class="footer-icon">
      <img src="@/assets/logo footer.png" alt="Logo de Haz Cosmética Mexicana" />
    </div>
    <div class="footer-services">
      <h3 class="footer-title">NUESTROS SERVICIOS</h3>
      <ul class="footer-list">
        <li>Creación de Identidad de Marca</li>
        <li>Amplia variedad de artículos en nuestro catálogo</li>
        <li>Diversidad en el Diseño de Envases</li>
      </ul>
    </div>
    <div class="footer-contact">
      <h3 class="footer-title">CONTÁCTANOS</h3>
      <p>Email: <a class="cont" href="mailto:ventas@hazcosmeticamexicana.com">ventas@hazcosmeticamexicana.com</a></p>
      <p>WhatsApp: <a class="cont" href="tel:+523311339494">+52 (33) 1133 9494</a></p>
      <!-- Íconos de redes sociales -->
      <div class="footer-social">
        <a href="https://www.facebook.com/tu_pagina_de_facebook" target="_blank"><i class="fab fa-facebook"></i></a>
        <a href="https://www.twitter.com/tu_perfil_de_twitter" target="_blank"><i class="fab fa-twitter"></i></a>
        <a href="https://www.linkedin.com/in/tu_perfil_de_linkedin" target="_blank"><i class="fab fa-linkedin"></i></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactoBlock',
};
</script>

<style scoped>
.footer-section {
  background-color: #4b5922;
  color: white;
  display: flex;
  justify-content: space-between;
  padding: 2rem 5vw;
  margin-top: 2rem;
  text-align: left;
}

.footer-services,
.footer-contact {
  width: 45%;
}

.footer-title {
  font-size: 1.2rem;
  font-weight: 700;
  margin-bottom: 1rem;
}

.footer-list {
  list-style: none;
  padding: 0;
  line-height: 1.8rem;
  font-size: .8rem;
}

.footer-contact p {
  line-height: 1.8rem;
}

.footer-social a {
  color: white;
  font-size: 1.5rem;
  margin: 0 0.5rem;
  text-decoration: none;
}

.footer-social a:hover {
  color: #ccc;
}
.footer-icon img {
  width: 5rem;
  padding-top: 3rem;
  padding-left: 6rem;
  padding-right: 8.5rem;
  position: flex;
}
.cont{
  color: rgba(50, 222, 176, 0.597);
  text-decoration: none;
}
</style>