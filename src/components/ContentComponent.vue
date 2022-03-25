<template>
    <div id="headerPart">
        <header>
            <img src="@/assets/img/logo.png" alt="isaac louzeiro logo">
            <h1>Web Design Art Gallery</h1>
            <p>by Isaac Louzeiro</p>
            <ul id="socialLinks">
                <li><a href="https://codepen.io/isaaclouzeiro/" title="Codepen Profile" target="_blank"><font-awesome-icon :icon="['fab', 'codepen']" /></a></li>
                <li><a href="https://github.com/IsaacLouzeiro" title="Github Profile" target="_blank"><font-awesome-icon :icon="['fab', 'github']" /></a></li>
                <li><a href="https://www.linkedin.com/in/isaac-louzeiro/" title="Linkedin Profile" target="_blank"><font-awesome-icon :icon="['fab', 'linkedin']" /></a></li>
                <li><a href="https://isaaclouzeiro.dev.br/" title="Website Portfolio" target="_blank"><font-awesome-icon :icon="['fas', 'window-maximize']" /></a></li>
            </ul>
        </header>

        <nav id="navbar">
            <ul class="nav">
                <li><a id="illustrationsLink" href="#" class="selected" @click="illustrationsFunc()">Illustrations</a></li>
                <li><a id="uiDesignLink" href="#" @click="uiDesignFunc()">UI/UX Design</a></li>
                <li><a id="webToolsLink" href="#" @click="webToolsFunc()">Web Tools</a></li>
            </ul>
        </nav>
    </div>

    <main>
        <ul>
            <li v-show="arrayIllustrations" v-for="item in illustrations" :key="item.illustrations">
                <img :src="item.img" :alt="item.title">
                <div id="headerProj">
                    <a :href="item.url" target="_blank"><font-awesome-icon :icon="['fab', 'codepen']" /></a>
                </div>
                <p>{{ item.title }}</p>
            </li>

            <li v-show="arrayUiDesign" v-for="item in uiDesign" :key="item.uiDesign">
                <img :src="item.img" :alt="item.title">
                <div id="headerProj">
                    <a :href="item.url" target="_blank"><font-awesome-icon :icon="['fab', 'codepen']" /></a>
                </div>
                <p>{{ item.title }}</p>
            </li>

            <li v-show="arrayWebTools" v-for="item in webTools" :key="item.webTools">
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
            webTools: Array,
        },
        data() {
            return {
                arrayIllustrations: 1,
                arrayUiDesign: 0,
                arrayWebTools: 0,
            }
        },
        methods: {
            illustrationsFunc() {
                document.getElementById('illustrationsLink').classList.add('selected');
                document.getElementById('uiDesignLink').classList.remove('selected');
                document.getElementById('webToolsLink').classList.remove('selected');

                this.arrayIllustrations = 1;
                this.arrayUiDesign = 0;
                this.arrayWebTools = 0;
            },
            uiDesignFunc() {
                document.getElementById('uiDesignLink').classList.add('selected');
                document.getElementById('illustrationsLink').classList.remove('selected');
                document.getElementById('webToolsLink').classList.remove('selected');
                
                this.arrayIllustrations = 0;
                this.arrayUiDesign = 1;
                this.arrayWebTools = 0;
            },
            webToolsFunc() {
                document.getElementById('webToolsLink').classList.add('selected');
                document.getElementById('illustrationsLink').classList.remove('selected');
                document.getElementById('uiDesignLink').classList.remove('selected');
            
                this.arrayIllustrations = 0;
                this.arrayUiDesign = 0;
                this.arrayWebTools = 1;
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../assets/sass/colors.scss';

    #headerPart {
        width: 100%;
        text-align: center;

        header {
            height: 200px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;

            img { width: 73px; }
            h1 { font-size: 23px; margin-top: 5px; }
            p { font-size: 18px; margin: 5px 0; font-weight: 600; }

            #socialLinks {
                list-style-type: none;
                li { 
                    display: inline-block;
                    font-size: 24px;
                    margin: 5px;

                    a { color: $color3; &:hover { color: $color4; } }
                }
            }
        }

        #navbar {
            .nav {
                list-style-type: none;
                height: 60px;
                display: flex;
                align-items: flex-end;
                justify-content: center;

                li {
                    display: inline-block;
                    margin: 0 6px;
                    
                    a { 
                        display: inline-block;
                        color: $color1; 
                        font-weight: bold; 
                        text-decoration: none;
                        padding: 8px 0; 
                        border-top: 3px solid;
                        border-color: $color5;

                        &:hover {
                            border-color: $color1;
                        }

                        &.selected {
                            border-color: $color4;
                        }
                    }
                }
                
                @media only screen and (max-width: 360px) {
                    font-size: .9em;
                }
            }
        }
    }

    main {
        width: 100%;
        max-width: 1140px;
        margin: 10px auto auto auto;
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
                    height: 25%;
                    position: relative;
                    z-index: 2;
                    background-image: linear-gradient(rgba($color1, .4), rgba($color1, 0));
                    display: flex;
                    justify-content: flex-end;
                    padding-top: 5px;
                    padding-right: 10px;

                    a {
                        color: $color4;
                        font-size: 1.5em;
                        filter: drop-shadow(0 0 2px rgba($color2, .8));
                    }
                }
                
                img {
                    position: absolute;
                    width: 100%;
                    height: 100%;
                    opacity: .9;

                    &:hover {
                        opacity: 1;
                    }
                }

                p {
                    position: absolute;
                    z-index: 2;
                    width: 100%;
                    text-align: center;
                    bottom: 5px;
                    font-weight: 600;
                    color: $color1;
                    text-shadow: 1px 1px 1px $color5;
                }
            }
        }
    }
</style>