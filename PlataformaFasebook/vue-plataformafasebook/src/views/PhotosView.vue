<template>
  <section>
    <h2>Fotos</h2>
    <div class="photo-grid">
      <img v-for="(foto, i) in fotos" :key="i" :src="foto" />
    </div>
  </section>
</template>

<script setup>
const fotos = [
  new URL('@/assets/foto1.jpg', import.meta.url).href,
  new URL('@/assets/foto2.jpg', import.meta.url).href,
  new URL('@/assets/foto3.jpg', import.meta.url).href
]
</script>
