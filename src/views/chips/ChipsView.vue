<template>
  <div class="ChipsView">
    <div class="wrapper">
      <div class="chips">
        <chip
          name="All"
          active
        />
        <chip
          name="Music"
        />
        <chip
          name="Playlists"
        />
        <chip
          name="Philippine Music"
        />
        <chip
          name="Mixes"
        />
        <chip
          name="Design Course"
        />
        <chip
          name="Live"
        />
        <chip
          name="Developer"
        />
        <chip
          name="Flutter"
        />
        <chip
          name="HTML"
        />
        <chip
          name="CSS"
        />
        <chip
          name="JavaScript"
        />
        <chip
          name="Dart"
        />
        <chip
          name="VueJS"
        />
        <chip
          name="NodeJS"
        />
        <chip
          name="MySQL"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Chip from '@/components/chip.vue'
export default {
  name: 'ChipsView',
  components: { Chip }
}
</script>

<style lang="scss" scoped>
  @import './styles/ChipsView.scss';
</style>
