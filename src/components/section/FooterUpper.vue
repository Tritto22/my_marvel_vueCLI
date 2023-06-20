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
                    <img :src="link.path" :alt="link.name" class="w-100">
                </div>
                <div class="info g-0">
                    <h5 class="text-uppercase m-0">{{link.name}}</h5>
                    <p>{{link.info}}</p>
                </div>
            </a>
        </div>
        <div class="social">
            <h5 class="text-uppercase m-0">follow marvel</h5>
            <div class="follow">
                <font-awesome-icon :icon="['fab', 'facebook']" class="icon"/>
                <font-awesome-icon :icon="['fab', 'twitter']" class="icon"/>
                <font-awesome-icon :icon="['fab', 'instagram']" class="icon"/>
                <font-awesome-icon :icon="['fab', 'tumblr']" class="icon"/>
                <font-awesome-icon :icon="['fab', 'youtube']" class="icon"/>
                <font-awesome-icon :icon="['fab', 'snapchat']" class="icon"/>
                <font-awesome-icon :icon="['fab', 'pinterest']" class="icon"/>
            </div>
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
                    path: require('../../assets/img/marvel_insider_logo.png'),
                    info: 'Get Rewarded for Being a Marvel Fan',
                    link: '#'
                },
                {
                    name: 'marvel unlimited',
                    path: require('../../assets/img/marvel_unlimited_logo.png'),
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
        color: $primary-txt-color-light;
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
            a:hover{
            color: #767676;
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
                    img{
                        object-fit: contain;
                        height: 40px;
                    }
                }
                .info{
                    padding-left: 30px;
                    p{
                        color: #696969;
                    }
                }
            }
        }
        .social{
            margin: 0 40px;
            .follow{
                margin-top: 10px;
                .icon{
                    width: calc(100% / 4);
                    margin-top: 20px;
                    font-size: 20px;
                    color: #767676;
                    cursor: pointer;
                    &:hover{
                        color: $primary-txt-color-light;
                    }
                }
            }
        }

    }
</style>