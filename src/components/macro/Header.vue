<template>
  <header>
      
      <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/768px-Spotify_logo_without_text.svg.png" alt="logo spotify">
      <div class="search-container">
            <SearchBar/>
      </div>
  </header>

</template>

<script>
import SearchBar from '../commons/SearchBar.vue';
export default {
    name: 'Header',
    components:{
        SearchBar
    },
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';

    header{
        width: 100%;
        height: 50px;
        background-color: $mainColor;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0 20px;

        img{
            height: 50px;
            padding: 10px 0;
        }

        .search-container{
            display: flex;
            justify-content: center;
        }
    }

</style>