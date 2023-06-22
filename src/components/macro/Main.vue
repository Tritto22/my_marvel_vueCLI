<template>
    <main>
        <Hero />
        <MainFirstSection />
    </main>
</template>

<script>
import Hero from '../section/Hero.vue'
import MainFirstSection from '../section/MainFirstSection.vue'

export default {
    name: 'Main',
    components: {
        Hero,
        MainFirstSection
    }
}
</script>

<style lang="scss" scoped>

</style>