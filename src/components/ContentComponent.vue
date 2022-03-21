<template>
    <main>
        <ul>
            <li v-for="item in illustrations" :key="item.illustrations">
                <img :src="item.img" :alt="item.title">
                <div id="headerProj">
                    <a :href="item.url" target="_blank"><font-awesome-icon :icon="['fab', 'codepen']" /></a>
                </div>
                <p>{{ item.title }}</p>
            </li>
        </ul>

        <ul>
            <li v-for="item in uiDesign" :key="item.uiDesign">
                <img :src="item.img" :alt="item.title">
                <div id="headerProj">
                    <a :href="item.url" target="_blank"><font-awesome-icon :icon="['fab', 'codepen']" /></a>
                </div>
                <p>{{ item.title }}</p>
            </li>
        </ul>

        <ul>
            <li v-for="item in webTools" :key="item.webTools">
                <img :src="item.img" :alt="item.title">
                <div id="headerProj">
                    <a :href="item.url" target="_blank"><font-awesome-icon :icon="['fab', 'codepen']" /></a>
                </div>
                <p>{{ item.title }}</p>
            </li>
        </ul>
    </main>
</template>

<script>
export default {
    name: 'ContentComponent',
    props: {
        illustrations: Array,
        uiDesign: Array,
        webTools: Array
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/sass/colors.scss';
    main {
        width: 100%;
        max-width: 1140px;
        margin: auto;
        padding-top: 10px;

        ul {
            list-style-type: none;
            display:  flex;
            flex-wrap: wrap;
            justify-content: center;

            li {
                width: 200px;
                height: 200px;
                position: relative;
                display: inline-block;
                margin: 2px;

                @media only screen and (max-width: 576px) {
                    width: 170px;
                    height: 170px;

                    p {
                        font-size: .9em;
                    }
                }

                @media only screen and (max-width: 360px) {
                    width: 150px;
                    height: 150px;

                    p {
                        font-size: .85em;
                    }
                }
                
                #headerProj {
                    width: 100%;
                    height: 20%;
                    position: relative;
                    z-index: 2;
                    background-image: linear-gradient(rgba($color1, .4), rgba($color1, 0));
                    display: flex;
                    justify-content: flex-end;
                    align-items: center;
                    padding-right: 10px;

                    a {
                        color: $color4;
                        font-size: 1.5em;
                    }
                }
                
                img {
                    position: absolute;
                    width: 100%;
                    height: 100%;
                }

                p {
                    position: absolute;
                    z-index: 2;
                    width: 100%;
                    text-align: center;
                    bottom: 5px;
                    font-weight: 600;
                    color: $color1;
                }
            }
        }
    }
</style>