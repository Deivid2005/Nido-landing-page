<template>
  <section class="events py-5">
    <div class="container">
      <div class="row">
        
        <div class="col-md-6 d-flex align-items-start">
          <h2>Próximos eventos</h2>
        </div>

        
        <div class="col-md-6">
          <div v-if="loading" class="text-center">Cargando eventos...</div>
          <div v-else-if="error" class="alert alert-danger">{{ error.message }}</div>
          <div v-else>
            <div class="card mb-3" v-for="event in events" :key="event.id">
              <div class="card-body">
                <h5 class="card-title">{{ event.title }}</h5>
                <p class="card-text text-muted">
                  {{ event.time }} — {{ event.description }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const events = [
  {
    id: 1,
    title: 'AI User Conference 2025 - Developer Day',
    time: '10:00 AM - 3:00 PM PDT',
    description: 'Gateway Pavilion - Piso 2',
  },
  {
    id: 2,
    title: 'AI Innovators Forum',
    time: '4:00 PM - 7:00 PM PDT',
    description: 'Mountain View, California',
  },
  {
    id: 3,
    title: 'Fine-Tune LLMs with SageMaker',
    time: '4:30 PM - 7:30 PM PDT',
    description: 'Amazon SJC25',
  },
];
</script>
