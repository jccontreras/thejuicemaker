<template>
  <div id="app" class="container-fluid">
    <nav class="navbar navbar-expand-lg navbar-light colorttop">
      <div class="col align-self-end">
        <a class="navbar-brand" href="https://www.facebook.com/thejuicemaker/" target="_blank">
          <img src="@/assets/logo/Facebook.png" width="24" height="24" alt="">
        </a>
        <a class="navbar-brand"
           href="https://www.instagram.com/thejuicemakercolombia/?igshid=5sime2d6pn1b"
           target="_blank">
          <img src="@/assets/logo/Instagram.png" width="24" height="24" alt="">
        </a>
        <a class="navbar-brand" href="https://www.youtube.com/channel/UCmgQAIr3-WOzWg8gABL__QQ" target="_blank">
          <img src="@/assets/logo/Youtube.png" width="24" height="24" alt="">
        </a>
      </div>
    </nav>
    <div class="row">
      <div id="top" class="col-2" style="max-width: 50%">
        <top/>
      </div>
      <div class="col" style="top: 20px">
        <button v-if="isclose" class="navbar-toggler" type="button" data-toggle="collapse"
                data-target="#navbarToggleExternalContent"
                aria-controls="navbarToggleExternalContent"
                aria-expanded="false" aria-label="Toggle navigation" style="position: relative"
                @click="openMenuJQ">
          <img src="@/assets/logo/openicon.png" style="max-height: 30px; max-width: 30px">
        </button>
        <button v-else class="navbar-toggler" type="button" data-toggle="collapse"
                data-target="#navbarToggleExternalContent"
                aria-controls="navbarToggleExternalContent"
                aria-expanded="false" aria-label="Toggle navigation" style="position: relative"
                @click="openMenuJQ">
          <img src="@/assets/logo/closeicon.png" style="max-height: 30px; max-width: 30px">
        </button>
        <router-view/>
      </div>
    </div>
    <down/>
    <modal-animacion/>
    <!--modal-abeas-data/-->
  </div>
</template>

<script>
import Top from '@/components/menu/Top.vue';
import Down from '@/components/footer/Down.vue';
import ModalAnimacion from '@/components/abeasdata/ModalAnimacion.vue';

const jq = require('jquery');

export default {
  name: 'App',
  components: {
    Top,
    Down,
    ModalAnimacion,
  },
  data() {
    return {
      isclose: false,
    };
  },
  methods: {
    openMenuJQ() {
      if (this.isclose === true) {
        jq('#top')
          .show(500);
        this.isclose = false;
      } else {
        jq('#top')
          .hide(500);
        this.isclose = true;
      }
    },
  },
  mounted() {
    // eslint-disable-next-line no-undef
    $('#staticBackdrop')
      .modal('show');
  },
};
</script>

<style lang="scss">
.container-fluid {
  background-color: #ffc700;
}
</style>
