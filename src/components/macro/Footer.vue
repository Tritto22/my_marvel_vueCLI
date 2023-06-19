<template>
    <footer>
        <FooterUpper/>
        <FooterLower/>
    </footer>
</template> 

<script>
import FooterUpper from '../section/FooterUpper.vue'
import FooterLower from '../section/FooterLower.vue'

export default {
    name: 'Footer',
    components: {
        FooterUpper,
        FooterLower
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';
    footer{
        background-color: $primary-bg-color-light;
        padding-top: 80px;
        padding-bottom: 30px;
    }
</style>