<template>
  <div class="layout">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'Layout',
  props: ['children']
}
</script>

<style lang="scss" scoped>
  @import "src/assets/styles/variables.scss";
  .layout {
    min-width: 320px;
    width: 100%;
    height: 100%;
    margin: 0 auto;

  }
</style>
