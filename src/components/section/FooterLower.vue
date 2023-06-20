<template>
    <nav>
        <ul>
            <li v-for="(link, i) in legelLinks" :key="i">
                <a :href="link.link">{{link.name}}</a>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
    nome: 'FooterLower',
    data() {
        return {
            legelLinks: [
                {
                    name: 'Terms of use',
                    link: '#'
                },
                {
                    name: 'Privacy Policy',
                    link: '#'
                },
                {
                    name: 'Interest-Based Ads',
                    link: '#'
                },
                {
                    name: 'EU Privacy Rights',
                    link: '#'
                },
                {
                    name: 'Cookie Policy',
                    link: '#'
                },
                {
                    name: 'License Agreement',
                    link: '#'
                },
                {
                    name: 'Manage Privacy Preferences',
                    link: '#'
                },
                {
                    name: '©2023 MARVEL',
                    link: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';

nav{
    max-width: 1240px;
    margin: auto;
    ul{
    display: flex;
    justify-content: center;
    padding: 0 20px;
        li{
            
            a{
                font-size: $lower-font-size;
                color: #696969;
                padding: 0 10px;
                margin-bottom: 10px;
            }
            a:hover{
                color: $primary-txt-color-light;
            }
        }
    }
}
</style>