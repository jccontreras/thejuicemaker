<template>
  <div class="modal fade" id="staticBackdrop" data-backdrop="static" data-keyboard="false"
       tabindex="-1" role="dialog" aria-labelledby="staticBackdropLabel" aria-hidden="true">
    <div class="modal-dialog">
      <div class="modal-content colormodal">
        <div class="modal-body">
          <div class="embed-responsive embed-responsive-16by9">
            <video id="anima" controls autoplay>
              <source src="@/assets/animaciones/animaciontjm.mp4" type="video/mp4">
            </video>
          </div>
        </div>
        <div class="modal-footer" style="border-style: none">
          <label style="color: black">
            Bienvenidos a The Juice Maker ....
          </label>
          <button type="button" class="btn btn-primary" data-dismiss="modal"
                  @click="pauseVideo">Continuar</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
const vid = document.getElementById('anima');

export default {
  name: 'ModalAnimacion',
  methods: {
    playVideo() {
      vid.play();
    },
    pauseVideo() {
      vid.pause();
    },
  },
  mounted() {
    // eslint-disable-next-line no-undef
    $('#anima')
      .play();
  },
};
</script>

<style lang="scss">
.colormodal {
  background-color: #ffd800;
  color: #ffd800;
}
</style>
