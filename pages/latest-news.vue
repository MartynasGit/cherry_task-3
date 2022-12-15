
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
                <div class="articles-item">
                    <img :src="b.media" :alt="b.title"  class="image-max-height"/>
                    <p>{{ b.title }}</p>
                    <p>{{ b.excerpt }}</p>
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
            this.articles = await fetch("http://localhost:3001/articles?_limit=5").then(res => res.json())
        },
        async getArticle(topic) {
            this.articles = await fetch(`http://localhost:3001/articles?topic=${topic}&_limit=5`).then(res => res.json())
        }
    }
}
</script>

<style scoped>
</style>