<template>
    <HeaderComponent />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';

export default {
  name: 'App',
  components: {
      HeaderComponent
  }
}
</script>

<style lang="scss">
    @import '/assets/sass/colors.scss';

    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&display=swap');

    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Montserrat', sans-serif;
    }

    body {
        width: 100%;
        background-color: $color5;
        color: $color1;
    }

    #app {
        width: 100%;
        max-width: 1140px;
        margin: auto;
    }
</style>
