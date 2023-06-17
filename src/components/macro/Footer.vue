<template>
    <footer>
        <FooterUpper/>
        <FooterLower/>
    </footer>
</template> 

<script>
import FooterUpper from '../section/FooterUpper.vue'
import FooterLower from '../section/FooterUpper.vue'

export default {
    name: 'Footer',
    components: {
        FooterUpper,
        FooterLower
    }
}
</script>

<style lang="scss" scoped>

</style>