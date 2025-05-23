<template>
  <section class="community py-5">
    <div class="container">
      <div class="row community__row">
        <div class="col-md-6">
          <h2>En NIDO, la comunidad es el motor de la innovación.</h2>
          <p>Eventos de networking periódicos para intercambio de experiencias.</p>
          <button class="btn btn-primary">Únete a la comunidad</button>
        </div>
        <div class="col-md-6 d-flex align-items-center justify-content-end">
          <img src="../assets/images/community.jpg" class="community__img" alt="Personas conversando" />
          <div class="community__dots">
            <span v-for="n in 4" :key="n" class="community__dot"></span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>