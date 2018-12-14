<template>
  <div id="app">
    <Navigation />
    <router-view/>
  </div>
</template>

<script>
// @ is an alias to /src
import Navigation from '@/components/Navigation.vue'

export default {
  name: 'navigation',
  components: {
    Navigation
  }
}
</script>

<style>
</style>
