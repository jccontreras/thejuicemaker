<template>
  <div id="carouselExampleIndicators" class="carousel slide carousel-fade carouselsize"
       data-ride="carousel">
    <ol class="carousel-indicators">
      <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
      <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
      <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
    </ol>
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="@/assets/img/pub1.jpeg" class="d-block w-100">
      </div>
      <div class="carousel-item">
        <img src="@/assets/img/pub2.jpeg" class="d-block w-100">
      </div>
      <div class="carousel-item">
        <img src="@/assets/img/pub3.jpeg" class="d-block w-100">
      </div>
    </div>
    <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button"
       data-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="sr-only">Previous</span>
    </a>
    <a class="carousel-control-next" href="#carouselExampleIndicators" role="button"
       data-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="sr-only">Next</span>
    </a>
  </div>
</template>

<script>
export default {
  name: 'Content1Home',
};
</script>

<style lang="scss">
.carouselsize {
  min-width: 100%;
  max-width: 100%;
  min-height: 80%;
  max-height: 80%;
  align-content: center;
}
</style>
