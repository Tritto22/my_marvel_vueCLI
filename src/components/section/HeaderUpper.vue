<template>
    <div class="header-upper">
        <div class="container">
            <div class="row">
                <div class="col-2 p-0">
                    <LogIn/>
                </div>
                <div class="col-7 p-0">
                    <Home/>
                </div>
                <div class="col-2 p-0">
                    <MarvelUnlimited/>
                </div>
                <div class="search">
                    <Search/>
                </div>
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
        border-bottom: 1px solid #2f2f2f;
        .container{
            padding: 0px 100px;
            .row{
                height: 100%;
            }
            .search{
                width:50px;
                padding: 0;
            }
        }
    }
    
</style>