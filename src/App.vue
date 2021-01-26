<template>
  <div id="app" class="container-fluid">
    <div class="row">
      <div v-if="isOpen" id="top" class="col-2" style="max-width: 50%"><top/></div>
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
    <!--down/>
    <modal-abeas-data/-->
  </div>
</template>

<script>
import Top from '@/components/menu/Top.vue';
import { mapMutations, mapState } from 'vuex';
import * as constants from '@/store/constants';

const $ = require('jquery');

window.$ = $;

export default {
  name: 'App',
  components: {
    Top,
  },
  data() {
    return {
      isclose: false,
    };
  },
  computed: {
    ...mapState({
      isOpen: (state) => state.Menu.isopen,
    }),
  },
  methods: {
    ...mapMutations({
      openMenu: constants.OPEN_MENU,
      closeMenu: constants.CLOSE_MENU,
    }),
    openMenuJQ() {
      if (this.isclose === true) {
        $('#top').show(300);
        this.isclose = false;
      } else {
        $('#top').hide(300);
        this.isclose = true;
      }
    },
  },
};
</script>

<style lang="scss">
.container-fluid {
  background-color: #ffc700;
}
</style>
