<template>
    <div class="container-nav w-100 m-auto d-flex">
        <div class="main-links d-flex">
            <a class="home">
                <img src="../../assets/img/Marvel_short_logo.png" alt="Marvel Short Logo">
            </a>
            <ul class="first-slot p-0">
                <li v-for="(link, i) in linkFirstSlot" :key="i">
                    <a :href="link.link" class="text-uppercase fw-bold text-decoration-none">{{link.name}}</a>
                </li>
            </ul>
            <ul class="second-slot p-0">
                <li v-for="(link, i) in linkSecondSlot" :key="i">
                    <a :href="link.link" class="text-uppercase text-decoration-none">{{link.name}}</a>
                </li>
            </ul>
        </div>
        <div class="pro-links">
            <a v-for="(link, i) in linksPro" :key="i" :href="link.link" class="pro-link d-flex">
                <div class="logo">
                    <img :src="link.img" :alt="link.name" class="w-100">
                </div>
                <div class="info g-0">
                    <h5 class="text-uppercase m-0">{{link.name}}</h5>
                    <p>{{link.info}}</p>
                </div>
            </a>
        </div>
        <div class="social">
            <h5 class="text-uppercase m-0">follow marvel</h5>
        </div>
    </div>
</template>

<script>
export default {
    nome: 'FooterUpper',
    data() {
        return {
            linkFirstSlot: [
                {
                    name: 'about marvel',
                    link: '#'
                },
                {
                    name: 'help/faqs',
                    link: '#'
                },
                {
                    name: 'careers',
                    link: '#'
                },
                {
                    name: 'internships',
                    link: '#'
                }
            ],
            linkSecondSlot: [
                {
                    name: 'advertising',
                    link: '#'
                },
                {
                    name: 'disney+',
                    link: '#'
                },
                {
                    name: 'marvelhq.com',
                    link: '#'
                },
                {
                    name: 'redeem digital comics',
                    link: '#'
                }
            ],
            linksPro: [
                {
                    name: 'marvel insider',
                    img: '../../assets/img/marvel_insider_logo.png',
                    info: 'Get Rewarded for Being a Marvel Fan',
                    link: '#'
                },
                {
                    name: 'marvel unlimited',
                    img: '../../assets/img/marvel_unlimited_logo.png',
                    info: 'Access Over 30,000+ Digital Comics',
                    link: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '../../assets/style/partials/variables.scss';
    a{
        color: $primary-txt-color-light;
        text-decoration: none;
    }
    h5{
        font-size: 14px;
    }
    .container-nav{
        max-width: 1240px;
        padding: 0 20px;
        .main-links{
            margin: 0 40px 70px 0;
            .home{
                margin-right: 60px;
                img{
                    width: 80px;
                }
            }
            .first-slot{
                margin-right: 60px;
            }
            ul{
                width: 150px;
                li{
                    margin-bottom: 12px;
                    cursor: pointer;
                }
            }
            
            a{
                font-size: 13px;
            }
        }
        .pro-links{
            margin: 0 40px;
            width: auto;
            .pro-link{
                padding-bottom: 30px;
                font-size: 13px;
                .logo{
                    width: 60px;
                }
                .info{
                    padding-left: 30px;
                    p{
                        color: #696969;
                    }
                }
            }
        }

    }
</style>