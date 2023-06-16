<template>
    <div class="header-upper">
        <div class="container">
            <div class="row">
                <div class="col-2 p-0">
                    <LogIn/>
                </div>
                <div class="col-7 p-0 debug"></div>
                <div class="col-2 p-0 debug"></div>
                <div class="col-1 p-0 debug"></div>
            </div>
        </div>
    </div>
</template>

<script>
import LogIn from '../elements/LogIn.vue'

export default {
    name: 'HeaderUpper',
    components: {
        LogIn
    }
}
</script>

<style lang="scss" scoped>
    // @import '../../assets/style/partials/variables.scss';
    .debug{
        height: 50px;
        border: 1px solid black;
        background-color: red;
    }
    .container{
        padding: 0px 100px;
        .row{
            height: 100%;
        }
    }
</style>