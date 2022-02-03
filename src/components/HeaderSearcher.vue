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
                <div class="results" v-for='result in results' :key='result.id'>
                    <img v-bind:src="'http://image.tmdb.org/t/p/w500/' +    result.poster_path" width='100px'>
                    <p>{{result.title}}</p>
                    <p>{{result.original_title}}</p>
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
        axios.get(`https://api.themoviedb.org/3/search/movie?api_key=e99307154c6dfb0b4750f6603256716d&query=${query}`).then(response => 
        { this.results = response.data.results 
        console.log(this.results) })
        
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
            .results {
                width: 1400px;
                display: flex;
                flex-wrap: wrap;
                margin: 0 auto ;

            }
        }
    }
</style>