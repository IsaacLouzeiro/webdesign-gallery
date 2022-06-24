<template>
    <ContentComponent :illustrations="illustrations" :webTools="webTools" :uiDesign="uiDesign" />
    <FooterComponent />
</template>

<script>
import ContentComponent from './components/ContentComponent.vue';
import FooterComponent from './components/FooterComponent.vue';

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
            ],

            uiDesign: [
                {
                    title: 'Open Spotify UI',
                    img: require('@/assets/img/art14.png'),
                    url: 'https://codepen.io/isaaclouzeiro/pen/zYRyoJw'
                },
                {
                    title: 'Hamburguer menu button interactive',
                    img: require('@/assets/img/art10.png'),
                    url: 'https://codepen.io/isaaclouzeiro/pen/gOopdyK'
                },
                {
                    title: 'Button hover effects',
                    img: require('@/assets/img/art11.png'),
                    url: 'https://codepen.io/isaaclouzeiro/pen/ExoVgox'
                },
                {
                    title: 'Toggle Button',
                    img: require('@/assets/img/art12.png'),
                    url: 'https://codepen.io/isaaclouzeiro/pen/jOYyZPM'
                }
            ],

            webTools: [
                {
                    title: 'Codepen challenge - Timekeeping',
                    img: require('@/assets/img/art9.png'),
                    url: 'https://codepen.io/isaaclouzeiro/pen/NWwLprP'
                },
                {
                    title: 'Color Picker',
                    img: require('@/assets/img/art13.png'),
                    url: 'https://codepen.io/isaaclouzeiro/pen/oNEzwQO'
                }
            ]
        } 
    },
    components: {
        ContentComponent,
        FooterComponent
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

    html,body, #app {
        width: 100%;
        height: 100%;
    }

    body {
        background-color: $color5;
        color: $color1;
    }

    #app {
        display: flex;
        flex-direction: column;
    }
</style>
