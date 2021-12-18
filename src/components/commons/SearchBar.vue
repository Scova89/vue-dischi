<template>
    <div class="search-bar">
        <form action="">
            <input type="text" placeholder="Search album" v-model="searchText">
            <button @click.prevent="$emit('search', searchText)">Search</button>
            <button>Reset</button>

        </form>
    </div>
</template>

<script>
export default {
    name: 'SearchBar',
    data() {
        return {
            searchText: ''
        }
    }
}
</script>

<style lang="scss" scoped>

</style>