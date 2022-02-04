<template>
<main>
        <div class="moviecontainer">
            <div class="moviesinfos" v-for='result in results' :key='result.id'>
                <img v-bind:src="'http://image.tmdb.org/t/p/w500/' +    result.poster_path" width='100px'>
                <div class="moviestxt">
                    <p>{{result.title}}</p>
                    <p>{{result.original_title}}</p>
                </div>
            </div>

    </div>
</main>

</template>

<script>


export default {
    data () {
        return{
            hover: false
        }
    },
    components: {
    },
    props: {
        results: [],
    },

}
</script>

<style lang="scss" >
    .moviecontainer {
        width: 100%;
        height: 1920px;
        background: rgb(77, 75, 75);
        display: flex;
        flex-wrap: wrap;
            .moviesinfos {
                width: 200px;
                height: 300px;
                color: whitesmoke;
                padding: 30px;
                margin: 50px;
                margin-top: 150px;
                img {
                   width: 200px;
                   transition: .5s; 
                   &:hover{
                       box-shadow: 0 0 35px rgba(218, 0, 0, 0.2);
                       cursor: pointer;
                       transition: .5s;
                       width: 250px;
                       .moviestxt {
                           text-align: center;
                       }
                   } 
                }
            } 
        
    }
    
</style>

