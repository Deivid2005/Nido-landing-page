<template>
<section class="logos-section">
  <div class="logo-grid">
    <img src="#" alt="Once Once">
    <img src="#" alt="Patio Santo">
    <img src="#" alt="Sushi Green">
    <img src="#" alt="La Consentida">
    <img src="#" alt="Florencia">
  </div>

  <p class="frase">“Construye tu visión, actúa sin esperar y conquista tu éxito.”</p>
</section>

<footer class="footer">
  <div class="footer-content">
    <div class="logo-footer">
      <img src="#" alt="NIDO logo">
    </div>
    <nav class="footer-nav">
      <a href="#">Inicio</a>
      <a href="#">Esto es NIDO</a>
      <a href="#">Comunidad</a>
      <a href="#">Programas</a>
    </nav>
    <div class="footer-social">
      <a href="#"><i class="fa-brands fa-facebook"></i></a>
      <a href="#"><i class="fa-brands fa-instagram"></i></a>
      <a href="#"><i class="fa-brands fa-twitter"></i></a>
      <a href="#"><i class="fa-brands fa-envelope"></i></a>
    </div>
    <p class="direccion">Avenida 123 #12 – 34 Cali, Colombia</p>
    <div class="footer-bottom">
      <p>© 2025 NIDO</p>
      <select>
        <option>English</option>
        <option>Español</option>
      </select>
    </div>
  </div>
</footer>

</template>

<style scoped>
.logos-section {
  text-align: center;
  padding: 60px 20px;
  background-color: #f9faff;
}

.logo-grid {
  display: flex;
  justify-content: center;
  gap: 30px;
  flex-wrap: wrap;
  margin-bottom: 40px;
}

.logo-grid img {
  width: 150px;
  height: auto;
  background-color: white;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
  padding: 10px;
}

.frase {
  font-size: 20px;
  color: #102a43;
  font-weight: 600;
}

.footer {
  background-color: #ffffff;
  padding: 40px 20px;
  border-top: 1px solid #ddd;
  text-align: center;
}

.footer-content {
  max-width: 1000px;
  margin: auto;
}

.footer-nav {
  margin: 20px 0;
}

.footer-nav a {
  margin: 0 15px;
  color: #222;
  text-decoration: none;
  font-weight: 500;
}

.footer-social a {
  margin: 0 10px;
  color: #222;
  font-size: 20px;
}

.direccion {
  margin-top: 15px;
  font-size: 14px;
  color: #555;
}

.footer-bottom {
  margin-top: 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  font-size: 13px;
  color: #888;
}

</style>