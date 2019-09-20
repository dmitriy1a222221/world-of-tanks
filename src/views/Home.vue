<template>
  <div class="home">
    <PopUpVideo/>
  </div>
</template>

<script>
import PopUpVideo from '@/components/PopUpVideo.vue'

export default {
  name: 'home',
  components: {
    PopUpVideo
  }
}
</script>

<style lang="scss" scoped>
  @import "src/assets/styles/variables";
</style>
