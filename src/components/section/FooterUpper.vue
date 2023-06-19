<template>
    <div class="container-nav w-100 m-auto">
        <div class="main-links d-flex">
            <a class="home">
                <img src="../../assets/img/Marvel_short_logo.png" alt="Marvel Short Logo">
            </a>
        </div>
        <div class="pro-links">

        </div>
        <div class="social">

        </div>
    </div>
</template>

<script>
export default {
    nome: 'FooterUpper'
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '../../assets/style/partials/variables.scss';
    .container-nav{
        max-width: 1240px;
        padding: 0 20px;
    }
    .home img{
        width: 80px;
    }
</style>