<template>
  <section>
    <h2>Cajas</h2>
    <div class="box-grid">
      <div class="box-card" v-for="box in cajas" :key="box">{{ box }}</div>
    </div>
  </section>
</template>

<script setup>
const cajas = ['📘 Logros académicos', '🛠 Proyectos', '🎮 Hobbies']
</script>
