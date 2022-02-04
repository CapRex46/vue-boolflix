<template>
<main>
        <div class="moviecontainer">
        <div class="moviestitles" v-for='result in results' :key='result.id'>
                <p>{{result.title}}</p>
                <p>{{result.original_title}}</p>
                <img v-bind:src="'http://image.tmdb.org/t/p/w500/' +    result.poster_path" width='100px'>
        </div>
    </div>
</main>

</template>

<script>


export default {
    components: {
        
    },
    props: {
        results: [],
    }
}
</script>

<style lang="scss" scoped>
    .moviecontainer {
        width: 100%;
        height: 900px;
        background: rgb(77, 75, 75);
        .moviestitles {
            width: 1400px;
            height: 600px;
            margin: 0 auto;
            .moviesimage {
                width: 200px;
                height: 300px;
                border: 1px solid white;
            }
        } 
    }
</style>