<template>
    <div class="searchnav">
        <div class="navcontent">
            <h1>
                BOOLFLIX
            </h1>
            <div>
                <label>Search title:  </label>
                <input type="text" v-model="query"  @keyup='$emit("query",getResult)'  placeholder="Search here.."/>
            </div>
        </div>
    </div> 
</template>

<script>

// commento 



export default {

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