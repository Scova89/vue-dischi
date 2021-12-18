<template>
    <div class="container">
        <div class="search-container">
            <SearchBar @search="searchAlbums"/>
        </div>
        <div class="card-container">
                <div class="box" v-for="(album, index) in albums" :key="index">
                    <DiscCard :info="album"/>
                </div>
        </div>
    </div>
  
</template>

<script>
import axios from 'axios';
import DiscCard from '../commons/DiscCard.vue';
import SearchBar from '../commons/SearchBar.vue';

export default {
    name: 'DiscList',
    components:{
        DiscCard,
        SearchBar
    },
    data() {
        return{
            albums: null
        }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            // handle success
            this.albums = response.data.response;
        })
        .catch(function (error) {
            // handle error
            console.log(error);
        });
    },
    methods: {
        searchAlbums(payload){
            console.log(payload)
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../../assets/style/partials/variables.scss';
    .container{
        .search-container{
            text-align: center;
            margin: 30px 0;
        }


        .card-container{
        width: 80%;
        display: flex;
        flex-wrap: wrap;
        margin: 0 auto;
        

            .box{
                text-align: center;
                width: 150px;
                height: 300px;
                background-color: $mainColor;
                margin: 30px;
            }
        }
    }
    
    
    
</style>