<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-md">
        <content1-home/>
      </div>
      <div class="col-md">
        <div class="card colorbody" style="max-width: 100%; border-style: none">
          <div class="card-body colorbody">
            <img src="@/assets/img/aboutus.png" style="max-width: 100%">
            <!--h1 class="card-title">Nuestra Filosof&iacute;a</h1>
            <h3 class="card-text" style="text-align: justify">
              Nos dedicamos a la creación, producción y grabación de música, su comercialización
              y distribución. Producimos artistas de géneros musicales como hip hop, trap, afro-
              beat, fusión entre otros.
              Cubrimos otros campos como la realización de videoclips, imagen, contenido, CD,
              programación de conciertos, entre otros.
            </h3-->
          </div>
        </div>
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

<style>
.colorbody {
  background-color: #ffc700;
  color: black;
}
</style>
