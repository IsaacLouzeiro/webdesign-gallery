<template>
    <HeaderComponent />
    <ContentComponent :illustrations="illustrations" />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import ContentComponent from './components/ContentComponent.vue';

export default {
    name: 'App',
    data() {
        return {
            illustrations: [
                {
                    title: 'Avatar Pixel Art',
                    img: require('@/assets/img/art2.png'),
                    url: 'https://codepen.io/isaaclouzeiro/pen/vYpYVVY'
                },
                {
                    title: 'Sunflower Pixel Art',
                    img: require('@/assets/img/art3.png'),
                    url: 'https://codepen.io/isaaclouzeiro/pen/OJzLBvb'
                },
                {
                    title: 'Interior Pixel Art',
                    img: require('@/assets/img/art4.png'),
                    url: 'https://codepen.io/isaaclouzeiro/pen/yLPmZwQ'
                },
                {
                    title: 'Toucan',
                    img: require('@/assets/img/art5.png'),
                    url: 'https://codepen.io/isaaclouzeiro/pen/ZEadPoW'
                },
                {
                    title: 'Night Sky',
                    img: require('@/assets/img/art6.png'),
                    url: 'https://codepen.io/isaaclouzeiro/pen/vYWqeKK'
                },
                {
                    title: 'Coffee Cup',
                    img: require('@/assets/img/art7.png'),
                    url: 'https://codepen.io/isaaclouzeiro/pen/wvPOxOg'
                },
                {
                    title: 'Corações (Hearts)',
                    img: require('@/assets/img/art8.png'),
                    url: 'https://codepen.io/isaaclouzeiro/pen/XWeEPeV'
                },
            ]
        } 
    },
    components: {
        HeaderComponent,
        ContentComponent
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
