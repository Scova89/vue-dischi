<template>

  <div class="card-container">
        <div class="box">
            <DiscCard/>
        </div>
        
      
  </div>
</template>

<script>
import DiscCard from '../commons/DiscCard.vue';
export default {
    name: 'DiscList',
    components:{
        DiscCard
    }
}
</script>

<style lang="scss" scoped>
    @import '../../assets/style/partials/variables.scss';
    .card-container{
        display: flex;
        flex-wrap: wrap;

        .box{
            text-align: center;
            width: 150px;
            height: 250px;
            background-color: $mainColor;
            margin: 30px;
        }
    }
    
    
</style>