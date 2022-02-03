<template>
  <div id="app">
    <header-searcher/>
    <movies-box/>
  </div>
</template>

<script>

import HeaderSearcher from './components/HeaderSearcher.vue'
import MoviesBox from './components/MoviesBox.vue'

export default {
  name: 'App',
  components: {
    HeaderSearcher,
    MoviesBox,
  }
}
</script>

<style lang="scss">
  @import './style/main.scss'
</style>
