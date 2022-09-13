<template>
  <div>
    <h1>{{ titulo }}</h1>
    <h3>{{ subtitulo }}</h3>
  </div>
</template>

<script>
export default {
  name: 'Titulo',
  data() {
    return {
      titulo: '',
      subtitulo: '',
    }
  },
  props: [{
    titulo: { type: String, required: true },
    subtitulo: { type: String, required: false },
  }]
}
</script>
