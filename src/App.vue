<template>
  <div id="app">
    <header-searcher @query="getResult"/>
    <movies-box :results="results"/>
  </div>
</template>

<script>

import axios from 'axios'
import HeaderSearcher from './components/HeaderSearcher.vue'
import MoviesBox from './components/MoviesBox.vue'

export default {
  data () {
    return {
      results: [],
    }
  },
  methods: {
    getResult(query) {
        axios.get(`https://api.themoviedb.org/3/search/movie?api_key=e99307154c6dfb0b4750f6603256716d&query=${query}`).then(response => 
        { this.results = response.data.results 
        console.log(this.results) });
        
        axios.get(`https://api.themoviedb.org/3/search/tv?api_key=e99307154c6dfb0b4750f6603256716d&language=it_IT&query=${query}`).then(response => 
        { this.results = response.data.results 
        console.log(this.results)});
    }
  },
  name: 'App',
  components: {
    HeaderSearcher,
    MoviesBox,
  }
}
</script>

<style lang="scss">
  @import './style/main.scss';
  @import url('https://use.fontawesome.com/releases/v5.7.1/css/all.css');
</style>
