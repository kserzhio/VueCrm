<template>
  <div id="app">
    <component :is="layout">
      <router-view/>
    </component>
  </div>
</template>
<script>
import LoginLayout from './layouts/LoginLayout'
import MainLayout from './layouts/MainLayout'
export default {
  computed: {
    layout () {
      return (this.$route.meta.layout || 'empty') + '-layout'
    }
  },
  comments: {
    LoginLayout,
    MainLayout
  }
}
</script>

<style lang="less">
@import "~materialize-css/dist/css/materialize.min.css";
@import "assets/index.css";
</style>
