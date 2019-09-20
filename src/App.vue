<template>
  <div id="app">
    <Layout>
      <router-view/>
    </Layout>
  </div>
</template>

<script>
import Layout from '@/components/Layout/index'
export default {
  name: 'App',
  components: {
    Layout
  }
}
</script>

<style lang="scss">
  @import "assets/styles/fonts";
  @import "assets/styles/reset";
</style>
