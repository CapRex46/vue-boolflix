<template>
    <div class="searchnav">
        <div class="navcontent">
            <h1 class="titlearea">
                BOOLFLIX
            </h1>
            <div class="searcharea">
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
        height: 80px;
        .navcontent {
            width: 1400px;
            margin: 0 auto;
            color: rgb(199, 59, 59);
            display: flex;
            justify-content: space-between;
            padding-top: 20px;
            input[type=text] {
                padding: 2px 20px;
                margin: 8px 0;
                box-sizing: border-box;
                border-radius: 4px;
                 background-color: rgb(77, 75, 75);
                 color: whitesmoke;
                }
        }
    }
</style>