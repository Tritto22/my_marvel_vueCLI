<template>
    <div class="header-upper">
        <div class="container-nav d-flex justify-content-between m-auto">
            <div class="left-nav">
                <LogIn/>
            </div>
            <div class="center-nav">
                <Home/>
            </div>
            <div class="right-nav d-flex">
                <MarvelUnlimited/>
                <Search/>
            </div>
        </div>
    </div>
</template>

<script>
import LogIn from '../elements/LogIn.vue'
import Home from '../elements/Home.vue'
import MarvelUnlimited from '../elements/MarvelUnlimited.vue'
import Search from '../elements/Search.vue'

export default {
    name: 'HeaderUpper',
    components: {
        LogIn,
        Home,
        MarvelUnlimited,
        Search
    }
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '../../assets/style/partials/variables.scss';
    .header-upper{
        border-bottom: 1px solid #373737;
        .container-nav{
            height: 52px;
            max-width: 1200px;
        }
    }
    
</style>