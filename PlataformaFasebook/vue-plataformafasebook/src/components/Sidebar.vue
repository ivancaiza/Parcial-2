<template>
  <aside class="sidebar">
    <img src="@/assets/avatar.jpg" alt="Avatar" class="avatar" />
    <h3>{{ nombre }}</h3>
    <ul>
      <li>Información</li>
      <li>Amigos</li>
      <li><a href="#">Ver todo</a></li>
    </ul>
    <div class="friends-grid">
      <img v-for="(foto, i) in fotos" :key="i" :src="foto" alt="Amigo" />
    </div>
  </aside>
</template>

<script setup>
const nombre = 'Nombre del Usuario'
const fotos = [
  new URL('@/assets/foto1.jpg', import.meta.url).href,
  new URL('@/assets/foto2.jpg', import.meta.url).href,
  new URL('@/assets/foto3.jpg', import.meta.url).href
]
</script>
