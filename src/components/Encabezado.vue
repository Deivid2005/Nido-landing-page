<template>
  <!-- Esqueleto de la página -->
  <header class="bg-light border-bottom navbar-fixed">
    <div class="container-fluid">
      <nav class="navbar navbar-expand-lg navbar-light sticky-top">
        <!-- Logo -->
        <a class="navbar-brand ms-3" href="#">
          <img src="/img/logoNIdo2.jpeg" alt="Logo Nido" height="70" class="d-inline-block align-text-top" />
        </a>

        <!-- Mobile Toggle Button -->
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>

        <!-- Navigation Menu -->
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto me-3">
            <li class="nav-item">
              <a class="nav-link text-muted fw-medium" href="#" @click="handleNavigation('inicio')">Inicio</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-muted fw-medium" href="#" @click="handleNavigation('esto-es-nido')">Esto
                es NIDO</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-muted fw-medium" href="#" @click="handleNavigation('comunidad')">Comunidad</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-muted fw-medium" href="#" @click="handleNavigation('programas')">Programas</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-muted fw-medium" href="#" @click="handleNavigation('contactanos')">Contáctanos</a>
            </li>
          </ul>
        </div>
      </nav>
    </div>
  </header>

 <div class="contenedor-efecto">
  <div class="img-efecto">
    <img src="/img/fondo1.jpeg" alt="Imagen 1" class="original" />
    <img src="/img/fondo1-hover.jpeg" alt="Imagen 1 Hover" class="alternativa" />
  </div>
  <div class="img-efecto">
    <img src="/img/fondo3.jpeg" alt="Imagen 2" class="original" />
    <img src="/img/fondo2-hover.jpeg" alt="Imagen 2 Hover" class="alternativa" />
  </div>
  <div class="img-efecto">
    <img src="/img/fondo2.jpeg" alt="Imagen 3" class="original" />
    <img src="/img/fondo3-hover.jpeg" alt="Imagen 3 Hover" class="alternativa" />
  </div>
</div>




  <div class="cajaContent">
  
  <h5 class="enunciado">Con el apoyo de</h5>


   <div class="cajaLogo">

   <div class="cajaImg2">
    <img src="/img/GOBERNACION-DEL-VALLE-DEL-CAUCA.webp" alt="Gobernación del Valle del Cauca" class="imageLogo2">
   </div>

   <div class="cajaImg1">
    <img src="/img/logo-alcaldia-cali.png" alt="Logo Alcaldía de Cali" class="imageLogo1">
   </div>

   <div class="cajaImg3">
    <img src="/img/camara-de-comercio.webp" alt="Cámara de Comercio de Cali" class="imageLogo3">
   </div>
   
   </div>
  </div>
</template>



<script>
export default {
    name: 'NidoHeader',
    data() {
        return {
            isVisible: true,
            lastScrollY: 0,
            scrollThreshold: 10
        }
    },
    mounted() {
        window.addEventListener('scroll', this.handleScroll);
    },
    beforeUnmount() {
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
        handleScroll() {
            const currentScrollY = window.scrollY;

            // Si está en la parte superior, siempre mostrar
            if (currentScrollY <= this.scrollThreshold) {
                this.isVisible = true;
                this.lastScrollY = currentScrollY;
                return;
            }

            // Si está bajando, ocultar
            if (currentScrollY > this.lastScrollY && currentScrollY > this.scrollThreshold) {
                this.isVisible = false;
            }
            // Si está subiendo, mostrar
            else if (currentScrollY < this.lastScrollY) {
                this.isVisible = true;
            }

            this.lastScrollY = currentScrollY;
        },
        handleNavigation(route) {
            // Lógica de navegación
            console.log('Navegando a:', route);
        }
    }
}
</script>




<style scoped>
/* Navbar fijo con animación */
.navbar-fixed {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1030;
    transform: translateY(0);
    transition: transform 0.3s ease-in-out;
}

.navbar-hidden {
    transform: translateY(-100%);
}

/* Espaciado para compensar el navbar fijo */
body {
    padding-top: 80px;
}

/* Estilos personalizados adicionales */
.nav-link:hover {
    color: #495057 !important;
    transition: color 0.3s ease;
}

/* Espaciado personalizado para el logo */
.navbar-brand {
    margin-left: 20px;
}

/* Ajustes de espaciado para la navegación */
.navbar-nav .nav-link {
    margin-left: 1rem;
    margin-right: 1rem;
}

.contenedor-efecto {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  gap: 50px;
  margin: 125px;
  overflow: visible;
}

.img-efecto {
  background-color: white;
  border-radius: 10px;
  box-shadow: 0px 20px 40px rgba(0, 0, 255, 0.08);
  width: 230px;
  height: 280px;
  overflow: visible;
  position: relative;
  cursor: pointer;
  transition: box-shadow 0.3s ease;
}

/* Imagen original: color y tamaño fijo */
.img-efecto img.original {
  width: 230px;
  height: 280px;
  object-fit: cover;
  border-radius: 5px;
  transition: filter 0.3s ease, opacity 0.3s ease, transform 0.3s ease;
  filter: none;
  opacity: 1;
  position: relative;
  z-index: 1;
  background-color: transparent;
}

/* Imagen alternativa: más grande, separada visualmente */
.img-efecto img.alternativa {
  width: 500px; /* Aumentamos el tamaño */
  height: 400px; /* Más alta también */
  object-fit: contain;
  border-radius: 5px;
  position: absolute;
  top: -40px; /* Se eleva un poco para alejarse visualmente */
  left: 50%;
  transform: translateX(-50%);
  opacity: 0;
  transition: opacity 0.3s ease, transform 0.3s ease;
  z-index: 2;
  background-color: transparent;
  margin-inline: 60px; /* Espacio horizontal extra */
}

/* Al hacer hover en el contenedor, todas las originales excepto la que se hover se ponen en blanco y negro */
.contenedor-efecto:hover .img-efecto:not(:hover) img.original {
  filter: grayscale(100%);
  opacity: 0.6;
  transform: scale(0.9);
  z-index: 1;
}

/* La imagen original desaparece cuando está hover */
.img-efecto:hover img.original {
  opacity: 0;
  transform: scale(1);
  z-index: 0;
}

/* La imagen alternativa aparece grande y centrada con separación */
.img-efecto:hover img.alternativa {
  opacity: 1;
  transform: translateX(-50%) scale(1.1); /* Ligeramente más grande aún */
  z-index: 3;
}


.enunciado{
  color:darkblue;
  text-align: center;
  
}

.cajaContent{
  background-color: lightgray;
  padding: 80px;
}




.cajaImg1{
 background-color: white;
  border-radius: 15px;
  padding: 30px; /* Espacio interno para igualar tamaño visual */
  margin: 1px; /* Separación entre logos */
  box-shadow: 0px 10px 20px rgba(0, 0, 255, 0.15);

} 

.cajaImg2{
 background-color: white;
  border-radius: 15px;
  padding: 25px; /* Espacio interno para igualar tamaño visual */
  margin: 1px; /* Separación entre logos */
  box-shadow: 0px 10px 20px rgba(0, 0, 255, 0.15);

}


.cajaImg3{
 background-color: white;
  border-radius: 15px;
  padding: 23px; /* Espacio interno para igualar tamaño visual */
  margin: 1px; /* Separación entre logos */
  box-shadow: 0px 10px 20px rgba(0, 0, 255, 0.15);

}

.cajaLogo{
  display: flex;
  justify-content: center;  /* Centra horizontalmente */
  align-items: center;      /* Centra verticalmente */
  gap: 20px;                /* Espacio entre logos */
  flex-wrap: wrap;          /* Por si se reduce el ancho de pantalla */
  padding: 20px;
}
.imageLogo1{
  height: 75px;
  width: 75px;
}

.imageLogo2{
  height: 85px;
  width: 85px;
}

.imageLogo3{
  height: 85px;
  width: 79px;
}
/* Media queries para ajustes responsivos */
@media (max-width: 991.98px) {
    .navbar-brand {
        margin-left: 0.75rem;
    }

    .navbar-nav {
        margin-top: 1rem;
    }

    .navbar-nav .nav-link {
        margin-left: 0;
        margin-right: 0;
        padding: 0.5rem 0;
    }
}
</style>
