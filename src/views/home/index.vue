<template>
  <div class="home">
    <div class="home__wrap-cont">
      <div>
        <HeadSection />
        <FormBlock class="home__form-mob"/>
      </div>
      <div>
        <BottomInfo />
        <FooterBlock />
      </div>
    </div>
    <FormBlock class="home__form-desck" />
  </div>
</template>

<script>
import HeadSection from '@/views/home/components/HeadSection'
import FormBlock from '@/views/home/components/FormBlock'
import BottomInfo from '@/views/home/components/BottomInfo'
import FooterBlock from '@/views/home/components/FooterBlock'

export default {
  name: 'Home',
  components: {
    HeadSection,
    FormBlock,
    BottomInfo,
    FooterBlock
  }
}
</script>

<style lang="scss" scoped>
  @import "src/assets/styles/variables";

  .home {
    width: 100%;
    height: auto;
    min-height: 100%;

    &__form-mob {
      display: block;
    }
    &__form-desck {
      display: none;
    }
  }

  @media screen and (min-width: 1200px) {
    .home {
      display: flex;
      justify-content: space-between;

      &__wrap-cont {
        flex-grow: 2;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
      }

      &__form-mob {
        display: none;
      }
      &__form-desck {
        display: block;
      }
    }
  }
</style>
