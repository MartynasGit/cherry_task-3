
<template>
    <div>

        <h2 class="text-5xl">Latest News</h2>
        <div class="lg:flex  md:flex grid grid-cols-3 gap-1 lg:my-7 my-0">
            <div v-for="p in categories">
                <Category :category="p" @click="getArticle(p)" />
            </div>
        </div>
        <div class="articles-grid">
            <div v-for="b  in articles">
                <div>
                    <img :src="b.media" :alt="b.title"  class="image-max-height"/>
                    <p class="text-xl font-bold">{{ b.title }}</p>
                    <p class="text-sm">{{ b.excerpt }}</p>
                    <span color="text-gray-700">{{b.author}}</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            articles: [],
            categories: ["Politics", "Finance", "Tech", "Beauty", "Science", "Food", "Sport"],
        }
    },
    created() {
        this.fetchArticles()
    },
    methods: {
        async fetchArticles() {
            this.articles = await fetch("http://localhost:3001/articles?_limit=6").then(res => res.json())
        },
        async getArticle(topic) {
            this.articles = await fetch(`http://localhost:3001/articles?topic=${topic}&_limit=6`).then(res => res.json())
        }
    },
    transition: 'home',
    mode: 'out-in'
}
</script>

<style scoped>
</style>