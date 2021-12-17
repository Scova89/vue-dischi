<template>
    <div class="card">
         <img :src="info.poster" :alt="info.title">
         <h3>{{info.title}}</h3>
         <p>{{info.author}}</p>
         <p>{{info.year}}</p>
    </div>
</template>

<script>
export default {
    name: 'DiscCard',
    props: {
        info: Object
    }
}
</script>

<style lang="scss" scoped>

    .card{
        

        h3{
            text-transform: uppercase;
            color: white;
            margin-bottom: 20px;
        }

        p{
            color: rgba(255, 255, 255, 0.397);
            
        }

        img{
            padding: 15px;
            width: 100%;
            object-fit: cover;
        }
    }

    

</style>