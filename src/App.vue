<template>
  <div>
    <transition>
      <keep-alive>
        <router-view/>
      </keep-alive>
    </transition>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  components: {
  }
})

export default class App extends Vue {
}
</script>

<style lang="scss">

  @import url('https://fonts.googleapis.com/css2?family=Comfortaa:wght@300&display=swap');
 // Import Bulma's core
  @import "~bulma/sass/utilities/_all";
  // Set your colors
  //$primary: #C13584;
  //$primary-invert: findColorInvert($primary);
  $secondary: #833AB4;
  $secondary-invert: findColorInvert($secondary);
  $navbar-item-img-max-height: 4rem;
  $hr-background-color: $dark;
  $hr-height: 1px;
  $dimensions: 16 24 32 48 64 96 128 256 512 1024;

  // Setup $colors to use as bulma classes (e.g. 'is-secondary')
  $colors: (
          "white": ($white, $black),
          "black": ($black, $white),
          "light": ($light, $light-invert),
          "dark": ($dark, $dark-invert),
          "primary": ($primary, $primary-invert),
          "info": ($info, $info-invert),
          "success": ($success, $success-invert),
          "warning": ($warning, $warning-invert),
          "danger": ($danger, $danger-invert),
          "secondary": ($secondary, $secondary-invert)
  );
  // Links
  $link: $primary;
  $link-invert: $primary-invert;
  $link-focus-border: $primary;
  // Import Bulma and Buefy styles
  @import "~bulma";
  // @import "~buefy/src/scss/buefy";

  // Typography
  h1, h2, span, p, b, a {
    font-family: 'Comfortaa';
  }

  // Default Styles
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }
</style>