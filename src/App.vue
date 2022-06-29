<template>
  <div id="app">
    <nav-view />
    <router-view />
  </div>
</template>

<script>
import NavView from '@/views/nav/NavView'
export default {
  name: 'App',

  components: {
    NavView
  },

  computed: {
    mediaPreference () {
      const hasDarkPreference = window.matchMedia(
        '(prefers-color-scheme: dark)'
      ).matches

      if (hasDarkPreference) {
        return 'theme--dark'
      }
      return 'theme--light'
    }
  },

  mounted () {
    document.getElementsByTagName('html')[0].setAttribute('data-theme', this.mediaPreference)
  }
}
</script>

<style lang="scss">

  @import 'src/assets/styles/reset.scss';
  @import 'src/assets/styles/preset.scss';

  body {
    overflow-y: scroll;
  }

  ::-webkit-scrollbar {
    width: 10px;
  }

  ::-webkit-scrollbar-button {
    display: none;
  }
</style>
