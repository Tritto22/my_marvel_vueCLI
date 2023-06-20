<template>
    <main>
        <Hero />
    </main>
</template>

<script>
import Hero from '../section/Hero.vue'

export default {
    name: 'Main',
    components: {
        Hero
    }
}
</script>

<style lang="scss" scoped>
    main{
        height: 300px;
        background-color: beige;
    }
</style>