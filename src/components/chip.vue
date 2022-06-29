<template>
  <div
    class="chip"
    :class="{ 'chip--active': active }"
  >
    {{ name }}
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Chip',

  props: {
    name: {
      type: String,
      default: '',
      required: true
    },
    active: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style lang="scss" scoped>
  @import 'src/assets/styles/components/chip.scss';
</style>
