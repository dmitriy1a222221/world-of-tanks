<template>
  <div class="home">
    <div class="home__wrap-cont">
      <HeadSection />
      <FormBlock class="home__form-mob"/>
      <BottomInfo />
      <FooterBlock />
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

      &__form-mob {
        display: none;
      }
      &__form-desck {
        display: block;
      }
    }
  }
</style>
