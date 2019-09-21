<template>
  <transition name="fade">
    <div class="popup">
      <div
        class="popup__wrap-close"
        v-on:click="closePop"
      >
        <Close
          class="popup__close"
        />
      </div>
      <iframe
        class="popup__video"
        src="https://www.youtube.com/embed/CmgeAyzeG0I"
        frameborder="0"
        allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen>
      </iframe>
    </div>
  </transition>
</template>

<script>
import Close from '@/components/svgComponents/Close'

export default {
  name: 'PopUpVideo',
  props: ['showPop'],
  methods: {
    closePop: function () {
      const video = document.querySelector('.popup__video')
      if (this.showPop) {
        video.src = 'https://www.youtube.com/embed/CmgeAyzeG0I'
      } else {
        video.src = ''
      }

      this.$emit('closeVideo', {
        show: false
      })
    }
  },
  components: {
    Close
  }
}
</script>

<style scoped lang="scss">
  @import "src/assets/styles/variables";
  .popup {
    background-color: rgba(20, 22, 24, 0.8);
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 20;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;

    &__wrap-close {
      position: absolute;
      top: 20px;
      right: 20px;
      cursor: pointer;
    }

    &__close {
      width: 15px;
      height: 15px;
      fill: $text_color_2;
      transition: fill .2s;

      &:hover {
        fill: $text_color_10 !important;
      }
    }

    &__video {
      width: calc((1115 * 100%) / 1920);
      height: calc((631 * 100%) / 1025);
    }
  }

  .fade-enter-active, .fade-leave-active {
    transition: opacity .5s;
  }
  .fade-enter, .fade-leave-to {
    opacity: 0;
  }
</style>
