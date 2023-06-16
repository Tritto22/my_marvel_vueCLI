<template>
    <div class="log-in">
        <img src="../../assets/img/insider_short_logo.png" alt="Insider Short Logo">
        <a><strong id="sign-in">sign in</strong></a>
        <a><strong>i</strong></a>
        <a><strong id="join">join</strong></a>
    </div>
</template>

<script>
export default {
    name: 'LogIn'
}
</script>

<style lang="scss" scoped>
    @import '../../assets/style/partials/variables.scss';
    .log-in{
        border: 1px solid #2f2f2f;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100%;
        img{
            width: 20px;
        }
        strong{
            text-transform: uppercase;
            font-size: 12px;
            padding: 0 5px;
        }
    }
    // #join{
    //     border-left: 2px solid $primary-txt-color-light;
    // }
</style>