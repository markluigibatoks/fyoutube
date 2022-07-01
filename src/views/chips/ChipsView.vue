<template>
  <div class="ChipsView">
    <div class="wrapper">
      <div
        ref="scroll"
        class="chips"
      >
        <button
          v-if="prevActive"
          class="chips__button chips__button--prev"
          @click="prev()"
        >
          <svg
            viewBox="0 0 16 16"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
          >
            <g
              mirror-in-rtl=""
              class="style-scope yt-icon"
            >
              <path
                d="M10.15,13.35L4.79,8l5.35-5.35l0.71,0.71L6.21,8l4.65,4.65L10.15,13.35z"
                class="style-scope yt-icon"
              />
            </g>
          </svg>
        </button>

        <chip
          name="All"
          active
        />
        <chip name="Music" />
        <chip name="Playlists" />
        <chip name="Philippine Music" />
        <chip name="Mixes" />
        <chip name="Design Course" />
        <chip name="Live" />
        <chip name="Developer" />
        <chip name="Flutter" />
        <chip name="HTML" />
        <chip name="CSS" />
        <chip name="JavaScript" />
        <chip name="Dart" />
        <chip name="VueJS" />
        <chip name="NodeJS" />
        <chip name="MySQL" />
        <chip name="Basketball" />
        <chip name="Volleyball" />
        <chip name="Editing" />
        <chip name="Gaming" />
        <chip name="Electronics" />
        <chip name="iPhone" />
        <chip name="Apple" />
        <chip name="Orange" />
        <chip name="Mango" />
        <chip name="Fruits" />
        <chip name="Avocado" />
        <chip name="Soap" />
        <chip name="Dishes" />
        <chip name="Tang" />
        <chip name="Go" />
        <chip name="Go Lang" />
        <chip name="Java" />

        <button
          v-if="nextActive"
          class="chips__button chips__button--next"
          @click="next()"
        >
          <svg
            viewBox="0 0 16 16"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
          >
            <g
              mirror-in-rtl=""
              class="style-scope yt-icon"
            >
              <path
                d="M4.97,12.65L9.62,8L4.97,3.35l0.71-0.71L11.03,8l-5.35,5.35L4.97,12.65z"
                class="style-scope yt-icon"
              />
            </g>
          </svg>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import Chip from '@/components/chip.vue'
export default {
  name: 'ChipsView',
  components: { Chip },

  data () {
    return {
      prevActive: false,
      nextActive: false,
      maximumScrollWidth: 0,
      width: 0
    }
  },

  computed: {

  },

  mounted () {
    this.maximumScrollWidth = this.$refs.scroll.scrollWidth - this.containerWidth
    this.width = this.$refs.scroll.getBoundingClientRect().width

    this.prevActive = this.$refs.scroll.scrollLeft > 0
    this.nextActive = !(this.$refs.scroll.scrollLeft === this.maximumScrollWidth)
  },

  methods: {
    prev () {
      this.$refs.scroll.scrollLeft -= this.containerWidth
    },

    next () {
      this.$refs.scroll.scrollLeft += this.width
    }
  }
}
</script>

<style lang="scss" scoped>
@import "./styles/ChipsView.scss";
</style>
