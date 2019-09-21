<template>
  <div id="app" class="app">
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

  body {
    background-color: #141618;
    background: url("assets/image/wot-bg.jpg");
    background-size: cover;
  }

  .app {
    height: 100%;
  }
</style>
