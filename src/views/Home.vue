<template>
  <div class="container">
    <div class="row">
      <div class="col-md">
        <content1-home/>
      </div>
      <div class="col-md">
        <label>
          Nos dedicamos a la creación, producción y grabación de música, su comercialización
          y distribución. Producimos artistas de géneros musicales como hip hop, trap, afro-
          beat, fusión entre otros.
          Cubrimos otros campos como la realización de videoclips, imagen, contenido, CD,
          programación de conciertos, entre otros.
        </label>
      </div>
    </div>
  </div>
</template>

<script>
import Content1Home from '@/components/home/Content1Home.vue';

export default {
  name: 'Home',
  components: {
    Content1Home,
  },
};
</script>
