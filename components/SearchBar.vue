<template>
    <div class='search_bar'>
        <input
            type="text"
            placeholder="Rechercher"    
        >
    </div>
</template>

<script>
export default {
    name: 'SearchBar'

}
</script>

<style lang='scss'>
    .search_bar {
        width: 100%;
        height: 45px;
        background-color: #011627;

        input {
            height: 25px;
            width: 180px;
            background: #272222;
            margin-top: 8px;
            margin-left: 230px;
        }
    }
</style>
