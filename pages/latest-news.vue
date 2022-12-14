<template>
    <div>
        <h2 class="text-5xl">Latest News</h2>
        <div class="flex gap-1 my-7">
            <div v-for="p in categories">
                <Category :category="p" />
            </div>
        </div>
        <div class="grid lg:grid-cols-3 gap-10" v-for="b in articles">
            <p>{{b.title}}</p>
        </div>
    </div>
</template>

<script setup>
const categories = ["Politics", "Finance", "Tech", "Beauty", "Science", "Food", "Sports"];

const articles = await $fetch("http://localhost:3001/articles")


</script>

<style scoped>

</style>