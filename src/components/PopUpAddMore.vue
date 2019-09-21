<template>
  <transition name="fade">
    <div class="add-more">
      <div
        class="add-more__wrap-close"
        v-on:click="closePop"
      >
        <Close
          class="add-more__close"
        />
      </div>
      <div class="add-more__content">
        <h4 class="add-more__title">
          Тарифи
        </h4>
        <div class="add-more__wrap-link">
          <a
            target="_blank"
            href="https://alfabank.ua/storage/files/tarrifs-wargaming2019.pdf"
            class="add-more__link"
          >
            Тарифи
          </a>
          <a
            target="_blank"
            href="https://alfabank.ua/storage/files/1516807720-rules-co-brand-alfabank-ukrainepdf.pdf"
            class="add-more__link"
          >
            Правила Wargaming
          </a>
          <a
            target="_blank"
            href="https://alfabank.ua/storage/files/card-recharge-rules-wot.pdf"
            class="add-more__link"
          >
            Правила поповнення картки
          </a>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
import Close from '@/components/svgComponents/Close'

export default {
  name: 'PopUpAddMore',
  props: ['show', 'toggleShow'],
  methods: {
    closePop: function () {
      this.$emit('closePop', {
        show: false
      })
    }
  },
  components: {
    Close
  }
}
</script>

<style lang="scss" scoped>
  @import "src/assets/styles/variables";

  .add-more {
    width: 100%;
    height: 340px;
    background-color: $text_color_16;
    position: absolute;
    bottom: 0;
    left: 0;
    z-index: 10;
    transition: all .5s;

    &:before {
      content: '';
      display: block;
      position: absolute;
      bottom: 340px;
      width: 100%;
      height: 100vh;
      z-index: 9;
      background-color: $text_color_17;
    }

    &__wrap-close {
      position: absolute;
      top: 20px;
      right: 20px;
      cursor: pointer;
    }

    &__close {
      width: 15px;
      height: 15px;
    }

    &__content {
      margin-left: 20%;
      margin-top: 10%;
    }

    &__wrap-link {
      display: flex;
      flex-direction: column;
    }

    &__title {
      font-family: $font_title_1;
      font-size: 16px;
      color: $text_color_2;
      margin: 30px 0;
    }

    &__link {
      font-family: $font_title_2;
      font-size: 12px;
      line-height: 30px;
      color: $text_color_2;
      text-decoration: underline;
    }
  }

  .fade-enter-active, .fade-leave-active {
    transform: translateY(0);
  }
  .fade-enter, .fade-leave-to {
    transform: translateY(100%);
  }

</style>
