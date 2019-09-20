<template>
  <div class="bottom-info">
    <div class="bottom-info__item">
      <div class="bottom-info__b-icon">
        <img src="../../../assets/image/phone.svg" alt="icon" class="bottom-info__icon">
      </div>
      <p class="bottom-info__item-title">
        Швидке оформлення по телефону
      </p>
    </div>
    <div class="bottom-info__item">
      <div class="bottom-info__b-icon">
        <img src="../../../assets/image/card-icon.svg" alt="icon" class="bottom-info__icon">
      </div>
      <p class="bottom-info__item-title">
        Безкоштовна доставка кур'єром
      </p>
    </div>
    <div class="bottom-info__item">
      <div class="bottom-info__b-icon">
        <img src="../../../assets/image/vawes.svg" alt="icon" class="bottom-info__icon">
      </div>
      <p class="bottom-info__item-title">
        Безконтактні
        оплати
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BottomInfo'
}
</script>

<style lang="scss" scoped>
  @import "src/assets/styles/variables";

  .bottom-info {
    padding: 26px 20px;
    background-color: $text_color_12;

    &__item {
      display: flex;
      align-items: center;
      margin-bottom: 35px;

      &:last-child {
        margin-bottom: 0;
      }
    }

    &__b-icon {
      width: 48px;
      height: 48px;
      background-color: $text_color_13;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 16px;
    }

    &__item-title {
      font-family: $font_title_2;
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      line-height: 24px;
      letter-spacing: -0.24px;
      color: $text_color_2;
      width: 45%;
    }
  }

  @media screen and (min-width: 940px) {
    .bottom-info {
      padding: 43px 20px 43px 60px;
      display: flex;
      align-items: center;

      &__item {
        margin-bottom: 0;
      }
      &__item-title {
        width: 55%;
      }
    }
  }
</style>
