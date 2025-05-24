
<script setup>
import Encabezado from "./components/Encabezado.vue";
import Contenido from "./components/Contenido.vue";
import PieDePagina from "./components/PieDePagina.vue";
import Comunidad from "./components/Comunidad.vue";
import Eventos from "./components/Eventos.vue";
import PowerStartup from "./components/PowerStartup.vue"; // asegúrate de que la P y la S estén igual que el archivo

import cuboImg from './assets/cubo.png'; // Asegúrate de que esté en /src/assets
</script>

<template>
  <Encabezado />
  <Contenido />
  <img :src="cuboImg" alt="Cubo" style="position: absolute; top: 1420px; left: 50px; z-index: 1000;" />
  <Comunidad />
  <Eventos />
  <PowerStartup />
  <PieDePagina />
</template>
