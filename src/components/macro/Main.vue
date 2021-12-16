<template>
  <main>
      <DiscList/>
  </main>

</template>

<script>
import DiscList from '../section/DiscList.vue';
export default {
    name: 'Main',
    components:{
        DiscList,
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';

    main{
        height: 100vh;
        background-color: $secondaryColor;
        display: flex;
        align-items: center;
        justify-content: center;
    }

</style>