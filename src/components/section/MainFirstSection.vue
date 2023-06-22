<template>
    <section class="container-sections">
        <div class="container-section position-relative" v-for="(section, i) in arraySections" :key="i">
            <div class="jumbotron" :class="section.key">
                <img :src="section.logo" :alt="section.key" class="logo">
                <h4>{{ section.name }}</h4>
                <p>{{ section.description }}</p>
                <button class="fw-bold text-uppercase border-0">learn more</button>
            </div>
            <div class="articles d-flex position-absolute z-1 start-50 translate-middle-x w-100">
                <CardArticle v-for="(article,i) in section.articles" :key="i" :article="article"/>
            </div>
        </div>
    </section>
</template>
<script>
import CardArticle from '../elements/CardArticle.vue'
export default {
    name: 'MainFirstSection',
    components: {
        CardArticle
    },
    data(){
        return{
            arraySections:[
                {
                    key: 'invasion',
                    name: null,
                    logo: require('../../assets/img/main_section/invasion_logo.png'),
                    description: 'Who do you trust? Marvel Studios\' Secret Invasion, an Original series, is streaming June 21 on Disney+.',
                    articles: [
                        {
                            name: 'tv shows',
                            description: 'Movies to Watch on Disney+ Before \'Secret Invasion\'',
                            path: require('../../assets/img/main_section/article_1.png')
                        },
                        {
                            name: 'tv shows',
                            description: '\'Secret Invasion\': Explore New Posters from the Series',
                            path: require('../../assets/img/main_section/article_2.png')
                        },
                        {
                            name: 'tv shows',
                            description: '\'Secret Invasion\': Samuel L. Jackson Talks Nick Fury Stepping Out of the Shadows ',
                            path: require('../../assets/img/main_section/article_3.png')
                        },
                        {
                            name: 'tv shows',
                            description: 'Prepare for \'Secret Invasion\' With New \'Marvel Studios Legends\' on Disney+',
                            path: require('../../assets/img/main_section/article_4.png')
                        }
                    ]
                },
                {
                    key: 'romita',
                    name: 'Remembering John Romita Sr.',
                    logo: null,
                    description: 'We mourn the loss of a legend.',
                    articles: [
                        {
                            name: 'comics',
                            description: 'Marvel Mourns the Loss of John Romita Sr.',
                            path: require('../../assets/img/main_section/article_5.png')
                        },
                        {
                            name: 'comics',
                            description: 'Remembering John Romita Sr., 1930-2023',
                            path: require('../../assets/img/main_section/article_6.png')
                        },
                        {
                            name: 'comics',
                            description: 'Spotlight on John Romita Sr.',
                            path: require('../../assets/img/main_section/article_7.png')
                        }
                    ]
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.invasion{
    background-image: url('../../assets/img/main_section/bg_invasion.png');
}
.romita{
    background-image: url('../../assets/img/main_section/bg_john_romita.png');
}
section{
    .container-section{
        height: 800px;
    }
    .jumbotron{
        height: 560px;
        clip-path: polygon(0 0, 100% 0, 100% 90%, 0 100%);
        color: white;
    }
    .articles{
        max-width: 1179px;
        background-color: white;
        padding: 10px;
        bottom: 1px;
    }
}
</style>