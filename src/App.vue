import nidoLogo from '../assets/nido-logo.png'import nidoLogo from '../assets/nido-logo.png'<script setup>

import Encabezado from "./components/Encabezado.vue";
import Contenido from "./components/Contenido.vue";
import PieDePagina from "./components/PieDePagina.vue";
import Comunidad from "./components/Comunidad.vue";
import Eventos from "./components/Eventos.vue";
import powerStartup from "./components/powerStartup.vue";

</script>

<template>
  <Encabezado />
  <Contenido />
  <img src="../src/assets/cubo.png" alt="" style="position: absolute; top: 520px; left: 50px; z-index: 1000px;">
  <Comunidad />
  <Eventos />
  <powerStartup />
  <PieDePagina />
</template>

