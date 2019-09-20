<template>
  <div class="head-section">
    <img src="@/assets/image/Logo.svg" alt="logo" class="head-section__logo">
    <div class="head-section__main-info">
      <div class="head-section__btn-card">
        <div class="head-section__btn-circle">
          <img
            src="../../../assets/image/Vector.svg" alt="arrow" class="head-section__btn-arrow">
        </div>
      </div>
      <div class="head-section__main-info-text">
        <h1 class="head-section__title">
          Картка <span class="i-desck">&nbsp;<br></span>
          «World <span class="i-mobile">&nbsp;<br></span>
          of Tanks»
        </h1>
        <p class="head-section__descr">
          Здійснюй покупки  - отримуй <span class="i-mobile">&nbsp;<br></span>
          золото та інші бонуси <span class="i-mobile">&nbsp;<br></span>
          безкоштовно
        </p>
      </div>
    </div>
    <div class="head-section__sub-info">
      <div class="head-section__sub-info-wrap-item">
        <div class="head-section__sub-info-item">
          <h2 class="head-section__item-title">30 днів</h2>
          <p class="head-section__item-descr">преміум-аккаунта в подарунок</p>
        </div>
        <div class="head-section__sub-info-item">
          <h2 class="head-section__item-title">31 золота</h2>
          <p class="head-section__item-descr">
            за кожні витрачені 50 UAH <span class="i-mobile">&nbsp;<br></span>
            в Преміум-магазині
          </p>
        </div>
      </div>
      <div class="head-section__sub-info-wrap-item">
        <div class="head-section__sub-info-item">
          <h2 class="head-section__item-title">До 11,5 золота</h2>
          <p class="head-section__item-descr">за кожні витрачені 50 UAH</p>
        </div>
        <div class="head-section__sub-info-item">
          <h2 class="head-section__item-title">27 особистих резервів</h2>
          <p class="head-section__item-descr">для прискорення прокачування</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'HeadSection'
}
</script>

<style lang="scss" scoped>
@import "src/assets/styles/variables";

.i-mobile {
  display: inline;
}
.i-desck {
  display: none;
}

.head-section {
  width: 100%;
  background: url("../../../assets/image/bg.png");
  background-size: cover;
  padding: 36px 0 44px;

  &__logo {
    padding-left: 38px;
    margin-bottom: 59px;
  }

  &__main-info {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  &__btn-card {
    width: 335px;
    min-width: 335px;
    height: 211px;
    box-shadow: 0 0 45px -7px $text_color_4;
    background: url("../../../assets/image/card.png");
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 45px;
  }

  &__btn-circle {
    width: 80px;
    height: 80px;
    border: 7px solid $text_color_2;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    background: $text_color_3;
    opacity: 0.8;
    box-shadow: 0 0 30px 8px $text_color_3;

    &:hover {
      border-color: #EB5757
    }
  }

  &__btn-arrow {
    padding-left: 7px;
  }

  &__title {
    font-family: $font_title_1;
    font-size: 36px;
    line-height: 48px;
    text-align: center;
    color: $text_color_2;
    margin-bottom: 32px;
  }

  &__descr {
    width: 282px;
    padding: 10px 14px;
    background: $text_color_5;
    border-radius: 4px;
    font-family: $font_title_1;
    font-size: 14px;
    line-height: 20px;
    text-align: center;
    color: $text_color_1;
    margin-bottom: 42px;
  }

  &__sub-info-wrap-item {
    margin-bottom: 38px;

    &:last-child {
      margin-bottom: 0;
    }
  }

  &__sub-info {
    padding: 0 20px;
    margin: 0 auto;
  }

  &__sub-info-item {
    margin-bottom: 38px;

    &:last-child {
      margin-bottom: 0;
    }
  }

  &__item-title {
    font-family: $font_title_1;
    font-size: 24px;
    line-height: 28px;
    display: flex;
    align-items: center;
    color:$text_color_2;
    margin-bottom: 10px;
  }

  &__item-descr {
    font-family: $font_title_2;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 28px;
    color:$text_color_2;
    max-width: 260px;
  }
}

@media screen and (min-width: 940px) {
  .i-mobile {
    display: none;
  }
  .i-desck {
    display: inline;
  }

  .head-section {
    &__main-info {
      flex-direction: row-reverse;
      align-items: flex-start;
      justify-content: space-between;
      padding: 0 30px 0 60px;
      margin-bottom: 85px;
    }
    &__title {
      text-align: left;
    }
    &__descr {
      margin-bottom: 0;
      text-align: left;
      margin-right: 15px;
      width: auto;
    }
    &__btn-card {
      margin-bottom: 0;
    }
    &__sub-info {
      padding-left: 60px;
      display: flex;
    }
    &__sub-info-wrap-item {
      margin-right: 170px;
    }
  }
}
</style>
