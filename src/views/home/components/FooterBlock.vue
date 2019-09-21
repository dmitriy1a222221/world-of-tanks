<template>
  <div class="b-footer">
    <p class="b-footer__copiright">
      © 2018 АТ «Альфа-Банк» (Україна). <span class="inline-mobile">&nbsp;<br></span>
      Ліцензія НБУ №61 від 05.10.2011 р.
    </p>
    <p
      class="b-footer__add-more"
      v-on:click="togglePop"
    >
      Додатково
    </p>
    <PopUpAddMore
      v-show="statePop"
      v-on:closePop="togglePop"
    />
  </div>
</template>

<script>
import PopUpAddMore from '@/components/PopUpAddMore'

export default {
  name: 'FooterBlock',
  components: {
    PopUpAddMore
  },
  data: function () {
    return {
      statePop: false
    }
  },
  methods: {
    togglePop: function (data) {
      if (data.show) {
        this.statePop = data.show
      } else {
        this.statePop = !this.statePop
      }
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "src/assets/styles/variables";

  .inline-mobile {
    display: inline;
  }

  .b-footer {
    padding: 24px 20px 9px;
    position: relative;

    &__copiright {
      font-family: $font_title_2;
      font-style: normal;
      font-weight: normal;
      font-size: 14px;
      line-height: 19px;
      text-align: center;
      color: $text_color_15;
      opacity: 0.7;
    }

    &__add-more {
      font-family: $font_title_2;
      font-style: normal;
      font-weight: normal;
      font-size: 14px;
      line-height: 45px;
      color: $text_color_10;
      text-align: center;
      cursor: pointer;
    }
  }

  @media screen and (min-width: 940px) {
    .inline-mobile {
      display: none;
    }

    .b-footer {
      display: flex;
      align-items: center;
      padding: 22px 20px 22px 60px;

      &__copiright {
        margin-right: 4px;
      }
    }
  }

  @media screen and (min-width: 1700px) {
    .b-footer {
      padding: 22px 20px 22px 153px;

      &__copiright, &__add-more {
        font-size: 14px;
        line-height: 19px;
      }
    }
  }
</style>
