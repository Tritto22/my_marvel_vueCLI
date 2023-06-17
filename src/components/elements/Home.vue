<template>
    <div class="home m-auto position-absolute start-0 end-0">
        <a href="#">
            <img src="../../assets/img/Marvel_Logo.png" alt="Marvel Extend Logo">
        </a>
    </div>
</template>

<script>
export default {
    name: 'Home'
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
    .home{
        border: 1px solid #373737;
        width: 130px;
        height: 52px;
        img{
            height: 50px;
        }
    }
</style>