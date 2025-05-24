<template>
  <!-- Esqueleto de la página -->
  <header class="bg-light border-bottom navbar-fixed" :class="{ 'navbar-hidden': !isVisible }">
    <div class="container-fluid">
      <nav class="navbar navbar-expand-lg navbar-light">
        <!-- Logo -->
        <a class="navbar-brand ms-3" href="#">
          <img src="/nido-logo.png" alt="NIDO" height="40" class="d-inline-block align-text-top" />
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
