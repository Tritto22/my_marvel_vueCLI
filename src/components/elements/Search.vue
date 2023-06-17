<template>
    <div class="search d-flex justify-content-center align-items-center h-100">
        <a href="#">
            <font-awesome-icon :icon="['fas', 'magnifying-glass']" />
        </a>
    </div>
</template>

<script>
export default {
    name: 'Search'
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '../../assets/style/partials/variables.scss';
.search{
    border: 1px solid #2f2f2f;
    a{
        color:$primary-txt-color-light;
        font-size: 20px;
    }
}
</style>