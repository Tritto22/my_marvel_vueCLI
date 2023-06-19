<template>
    <nav>
        <ul>
            <li><a href="#">Terms of use</a></li>
            <li><a href="#">Terms of use</a></li>
            <li><a href="#">Terms of use</a></li>
            <li><a href="#">Terms of use</a></li>
            <li><a href="#">Terms of use</a></li>
            <li><a href="#">Terms of use</a></li>
            <li><a href="#">Terms of use</a></li>
            <li><a href="#">Terms of use</a></li>
        </ul>
    </nav>
</template>

<script>
export default {
    nome: 'FooterLower'
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';

ul{
    display: flex;
    li{
        text-decoration: none;
        a{
            color: $primary-txt-color-light;
        }
    }
}
</style>