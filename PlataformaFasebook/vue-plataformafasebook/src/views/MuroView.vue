<template>
  <section>
    <div class="post-box">
      <textarea v-model="nuevoPost" placeholder="Pon algo aquí..."></textarea>
      <div class="post-actions">
        <button>Adjuntar +</button>
        <button class="share-btn" @click="agregarPost">Compartir</button>
      </div>
    </div>

    <PostCard
      v-for="(post, i) in posts"
      :key="i"
      :autor="post.autor"
      :fecha="post.fecha"
      :contenido="post.contenido"
    />
  </section>
</template>

<script setup>
import { ref } from 'vue'
import PostCard from '@/components/PostCard.vue'

const nuevoPost = ref('')
const posts = ref([
  { autor: 'Nombre', fecha: 'Lunes a las 8:45pm', contenido: 'Estudiando para los parciales 😩📚' }
])

function agregarPost() {
  if (nuevoPost.value.trim()) {
    posts.value.unshift({
      autor: 'Nombre del Usuario',
      fecha: new Date().toLocaleString(),
      contenido: nuevoPost.value
    })
    nuevoPost.value = ''
  }
}
</script>
