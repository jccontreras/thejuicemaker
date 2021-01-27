<template>
  <div class="card cardhome" style="border: #e0d9d9">
    <div class="card-body">
      <div class="embed-responsive embed-responsive-21by9">
        <video controls autoplay>
          <source src="@/assets/animaciones/animaciontjm.mp4" type="video/mp4">
        </video>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContainerAnimacion',
};
</script>

<style lang="scss">
.cardhome {
  background-color: #ffc700;
  color: #ffc700;
}
</style>
