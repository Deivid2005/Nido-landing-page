<script setup>

import Encabezado from "./components/Encabezado.vue";
import Contenido from "./components/Contenido.vue";
import PieDePagina from "./components/PieDePagina.vue";
import Comunidad from "./components/Comunidad.vue";
import Eventos from "./components/Eventos.vue";

</script>

<template>
  <Encabezado />
  <!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>NIDO</title>
  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
  <div id="app"></div>
  <!-- Bootstrap JS -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  <script type="module" src="/src/main.js"></script>
</body>
</html>
  <Contenido />
  <Comunidad />
  <Eventos />
  <PieDePagina />
  
</template>

