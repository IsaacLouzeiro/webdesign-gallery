<template>
    <footer>
        <span>All rights reserved | &copy; Copyright 2022</span>
    </footer>
</template>

<script>
export default {
    name: 'FooterComponent'
}
</script>

<style lang="scss" scoped>
    @import '../assets/sass/colors.scss';
    footer {
        width: 100%;
        background-color: $color4;
        text-align: center;
        margin-top: 15px;
        padding: 12px;
        color: $color5;

        span {
            font-weight: 500;
            font-size: .9em;
        }
    }
</style>