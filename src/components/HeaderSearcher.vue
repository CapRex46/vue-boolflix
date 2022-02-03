<template>
    <div class="searchnav">
        <div class="navcontent">
            <h1>
                BOOLFLIX
            </h1>
            <div>
                <label>Search title:  </label>
                <input type="text" v-model="query"  @keyup="getResult(query)"  placeholder="Search here.."/>
            </div>

        </div>
    </div>
</template>

<script>

import axios from 'axios'

export default {
    data () {
    return {
      query: '',
      results: ''
    }
  },
  methods: {
    getResult(query) {
        axios.get('https://api.themoviedb.org/3/search/movie?  api_key=54db99dd2daf1d201355d467ba7c5a64query=' + query).then(response => { this.results = response.data.results })
        console.log(this.results)
    }
  },
}
</script>

<style lang="scss" scoped>
    .searchnav {
        width: 100%;
        background: black;
        .navcontent {
            width: 1400px;
            margin: 0 auto;
            color: rgb(199, 59, 59);
            display: flex;
            justify-content: space-between;
        }
    }
</style>