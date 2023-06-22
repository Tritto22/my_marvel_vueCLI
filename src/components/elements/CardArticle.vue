<template>
    <div class="card-article">
        <img :src="article.path" :alt="article.name">
        <div class="info">
            <h4>{{article.name}}</h4>
            <p>{{ article.description }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardArticle',
    props: {
        article: Object
    }
}
</script>

<style lang="scss" scoped>
    .card-article{
        width: calc(100% / 4);
        padding: 10px;
        img{
            object-fit: cover;
            width: 100%;
        }
        h4{
            text-transform: uppercase;
            font-size: 14px;
            font-weight: bold;
            color: #767676;
            margin-top: 20px;
        }
        p{
            font-size: 15px;
            font-weight: bold;
            cursor: pointer;
            margin-top: 8px;
        }
    }
</style>