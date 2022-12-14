<template>
    <div class="sm:px-20 sm:py-2">
        <header>
            <nav class=" mx-auto flex justify-between text-base p-3">
                <div>
                    <ul class="flex sm:gap-2 gap-2 md:gap-8" >
                        <li>
                            <NuxtLink class="sm:mr-5">=</NuxtLink>
                        </li>
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
                <div class="flex sm:gap-5">
                    <NuxtLink to="/contact" class="sm:mx-0 mx-2">Contact Us</NuxtLink>
                    <ColorMode />
                </div>
            </nav>
        </header>
        <div class="p-2 container">
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
</script>