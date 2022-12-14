
<template>
    <div>
        <h2 class="text-5xl">Latest News</h2>
        <div class="flex gap-1 my-7">
            <div v-for="p in categories">
                <Category :category="p" @click="getArticle(p)" />
            </div>
        </div>
        <div class="grid gap-10" v-for="b in articles">
            <p>{{ b.title }}</p>
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
            this.articles = await fetch("http://localhost:3001/articles?_limit=3").then(res => res.json())
        },
        async getArticle(topic) {
            this.articles = await fetch(`http://localhost:3001/articles?topic=${topic}&_limit=3`).then(res => res.json())
        }
    }
}
</script>

<style scoped>

</style>