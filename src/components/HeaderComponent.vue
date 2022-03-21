<template>
    <div id="headerComponent">
        <header>
            <img src="@/assets/img/logo.png" alt="isaac louzeiro logo">
            <h1>Webdesign Art Gallery</h1>
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
                <li><a href="#" class="selected">Illustrations</a></li>
                <li><a href="#">UI/UX Design</a></li>
                <li><a href="#">Web Tools</a></li>
            </ul>
        </nav>
    </div>
</template>

<script>
export default {
    name: 'HeaderComponent'
}
</script>

<style lang="scss" scoped>
    @import '../assets/sass/colors.scss';

    #headerComponent {
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
</style>