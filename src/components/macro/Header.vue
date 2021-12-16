<template>
  <header>
      <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/768px-Spotify_logo_without_text.svg.png" alt="logo spotify">
  </header>

</template>

<script>
export default {
    name: 'Header'
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

        img{
            height: 50px;
            padding: 10px;
        }
    }

</style>