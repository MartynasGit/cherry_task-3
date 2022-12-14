<template>
    <div>
        <h2 class="text-5xl">Latest News</h2>
        <div class="flex gap-1 my-10">
            <div v-for="p in categories">
                <Category :category="p" />
            </div>
        </div>
        <div class="grid lg:grid-cols-3 gap-10" v-for="b in articles">
            <!-- <div>
                <p>Number of the Day</p>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum harum hic ducimus, est obcaecati
                    vitae.</p>
            </div> -->
            

        </div>
    </div>
</template>

<script setup>
const categories = ["Politics", "Buisness", "Tech", "Arts", "Science", "Health", "Sports"]
</script>

<style scoped>

</style>