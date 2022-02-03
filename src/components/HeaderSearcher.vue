<template>
    <div class="searchnav">
        <div class="navcontent">
            <h1>
                BOOLFLIX
            </h1>
            <div>
                <label>Search title:  </label>
                <input type="text" v-model="search" placeholder="Search here.."/>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
    .searchnav {
        width: 100%;
        height: 80px;
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