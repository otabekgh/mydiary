<template>
  <component v-bind:is="layout"></component>
</template>

<script>
import AppLayout from '@/layouts/AppLayout'
import LoginLayout from '@/layouts/LoginLayout'

export default {
  name: 'App',
  computed: {
    layout () {
      return this.$store.getters.layout
    }
  },
  components: {
    'app-layout': AppLayout,
    'login-layout': LoginLayout
  }
}
</script>

<style>
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 0 16px;
  max-width: 700px;
}
.nav {
  margin-bottom: 10px;
}
.nav a.router-link-active {
  color: #000;
}
</style>
