<template>
    <div class="container px-16 pt-7">
        <header>
            <nav class="container mx-auto flex justify-between text-base">
                <div>
                    <ul class="flex gap-8">
                        <li><NuxtLink class="font-bold mr-5">=</NuxtLink></li>
                        <li>
                            <NuxtLink to="/">Home</NuxtLink>
                        </li>
                        <li>
                            <NuxtLink to="/latest-news">Latest News</NuxtLink>
                        </li>
                        <li>
                            <NuxtLink to="/reviews">Reviews</NuxtLink>
                        </li>
                    </ul>
                </div>
                <div class="flex gap-5">
                    <NuxtLink to="/contact">Contact Us</NuxtLink>
                    <ColorMode/>      
                </div>
            </nav>
        </header>
        <div class="mt-10">
            <slot></slot>
        </div>
    </div>
</template>
<style>
.router-link-exact-active {
    color: #b0695c;
}
</style>

<script setup>
const colorMode = useColorMode()
console.log(colorMode.preference)
</script>