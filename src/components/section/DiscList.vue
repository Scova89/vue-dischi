<template>

  <div class="card-container">
        <div class="box" v-for="(album, index) in albums" :key="index">
            <DiscCard :info="album"/>
        </div>
        
      
  </div>
</template>

<script>
import axios from 'axios';
import DiscCard from '../commons/DiscCard.vue';
export default {
    name: 'DiscList',
    components:{
        DiscCard
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
            this.albums = response.data;
        })
        .catch(function (error) {
            // handle error
            console.log(error);
        });
    }
}
</script>

<style lang="scss" scoped>
    @import '../../assets/style/partials/variables.scss';
    
    .card-container{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;


        .box{
            text-align: center;
            width: 150px;
            height: 250px;
            background-color: $mainColor;
            margin: 30px;
        }
    }
    
    
</style>