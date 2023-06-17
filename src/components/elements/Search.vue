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
    border-left: 1px solid #373737;
    border-right: 1px solid #373737;
    padding: 0 15px;
    a{
        color:$primary-txt-color-light;
        font-size: 16px;
    }
}
</style>