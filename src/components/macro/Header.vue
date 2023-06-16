<template>
    <header>
        <HeaderUpper/>
        <HeaderLower/>
    </header>
</template>

<script>
import HeaderUpper from '../section/HeaderUpper.vue'
import HeaderLower from '../section/HeaderLower.vue'

export default {
    name: 'Header',
    components: {
        HeaderUpper,
        HeaderLower
    }

}
</script>

<style lang="scss" scoped>
    @import 'bootstrap';
    @import '../../assets/style/partials/variables.scss';
    header{
        background-color: $primary-bg-color-light;
        color: $primary-txt-color-light;
    }
</style>