<template>
    <div class="marvel-unlimited d-flex justify-content-center align-items-center h-100">
        <img src="../../assets/img/unlimited_short_logo.png" alt="Unlimited Logo">
        <div class="description text-center">
            <a href="#" class="text-decoration-none text-uppercase fw-bold">marvel unlimited</a>
            <a href="#" class="text-decoration-none text-uppercase fw-bold d-block">subscribe</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MarvelUnlimited'
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '../../assets/style/partials/variables.scss';
    a{
        color:$primary-txt-color-light;
        font-size: $lower-font-size;
    }
    .marvel-unlimited{
        border: 1px solid #2f2f2f;
        img{
            height: 25px;
            margin: 0 10px;
        }
        .description{
            line-height: 0.9;
            & a:last-child{
                font-size: 10px;
            }
        }
    }
</style>