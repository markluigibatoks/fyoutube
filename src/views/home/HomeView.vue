<template>
  <div class="HomeView">
    <chips-view />
    <thumbnails-view />
  </div>
</template>

<script>
import ChipsView from '@/views//chips/ChipsView.vue'
import ThumbnailsView from '@/views//thumbnails/ThumbnailsView.vue'
// @ is an alias to /src

export default {
  name: 'HomeView',
  components: {
    ChipsView,
    ThumbnailsView
  }
}
</script>

<style>
  @import './styles/HomeView.scss';
</style>
