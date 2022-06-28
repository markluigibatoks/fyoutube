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
