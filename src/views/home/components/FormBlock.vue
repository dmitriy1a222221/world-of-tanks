<template>
  <div class="b-form">
    <h2 class="b-form__title">Замовити картку</h2>
    <form action="#" class="b-form__form">
      <input type="text" placeholder="Прізвище" class="b-form__input">
      <input type="text" placeholder="Ім’я" class="b-form__input">
      <input type="text" placeholder="По-батькові" class="b-form__input">
      <input type="text" placeholder="Номер мобільного телефону" class="b-form__input">
      <label class="container">
        <p class="container__text">
          Я погоджуюся з <a href="https://alfabank.ua/about/usloviya-oformleniya-onlajn-zayavki" target="_blank" class="text-red">умовами оформлення</a> онлайн-заявки
        </p>
        <input type="checkbox">
        <span class="checkmark"></span>
      </label>
      <div class="b-form__button">
        Відправити заявку
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'FormBlock'
}
</script>

<style lang="scss" scoped>
@import "src/assets/styles/variables";

.text-red {
  color: $text_color_4;
  text-decoration: none;
}

.b-form {
  padding: 62px 20px 40px;
  background-color: $text_color_6;
  display: flex;
  flex-direction: column;
  align-items: center;

  &__title {
    font-family: $font_title_1;
    font-size: 28px;
    line-height: 36px;
    color: $text_color_2;
    display: block;
    margin: 0 auto 40px;
    text-align: center;
  }

  &__form {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
  }

  &__input {
    background: none;
    border: none;
    border-bottom: 0.5px solid $text_color_2;
    max-width: 335px;
    width: 100%;
    font-family: $font_title_3;
    font-size: 17px;
    line-height: 30px;
    color: $text_color_2;
    margin-bottom: 44px;
    outline: none;

    &:focus {
      outline: none;
    }

    &:last-child {
      margin-bottom: 42px;
    }
  }

  &__button {
    width: 335px;
    height: 56px;
    background: $text_color_10;
    border-radius: 6px;
    font-family: $font_title_3;
    font-size: 17px;
    line-height: 56px;
    text-align: center;
    color: $text_color_2;
    margin-top: 52px;
    transition: all .3s;
    user-select: none;

    &:hover {
      box-shadow: 0 8px 16px $text_color_11;
    }
  }

  .container {
    display: block;
    position: relative;
    cursor: pointer;
    user-select: none;
    box-sizing: border-box;
    max-width: 335px;

    &__text {
      font-family: $font_title_4;
      font-size: 14px;
      line-height: 24px;
      letter-spacing: -0.24px;
      color: $text_color_2;
      padding-left: 35px;
    }

    &>input {
      position: absolute;
      opacity: 0;
      cursor: pointer;
      height: 0;
      width: 0;
    }

    &>input:checked ~ .checkmark:after {
      display: block;
    }

  }
  .checkmark {
    position: absolute;
    top: 0;
    left: 0;
    height: 22px;
    width: 22px;
    border-radius: 3px;
    border: 2px solid $text_color_7;
    background-color: transparent;
    box-sizing: border-box;

    &:after {
      content: "";
      position: absolute;
      display: none;
    }

    &:after {
      left: 5px;
      top: 1px;
      width: 5px;
      height: 10px;
      border: solid $text_color_9;
      border-width: 0 3px 3px 0;
      transform: rotate(45deg);
    }
  }
}

@media screen and (min-width: 1200px) {
  .b-form {
    &__title {
      text-align: left;
    }
  }
}

@media screen and (min-width: 1700px) {
  .b-form {
    padding: 60px 45px 40px 45px;
    align-items: flex-start;

    &__form {
      align-items: flex-start;
    }

    &__title {
      font-size: 32px;
      line-height: 36px;
    }

    &__input {
      font-size: 18px;
      max-width: 300px;

      &:last-child {
        margin-bottom: 42px;
      }
    }

    &__button {
      margin-top: 25px;
    }

    .container__text {
      max-width: 80%;
    }
  }
}

@media screen and (min-width: 1920px) {
  .b-form {
    padding: 60px 162px 40px 66px;
  }
}
</style>
