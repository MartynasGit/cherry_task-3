<template>
    <div>
        <header>
            <nav>
                <div>
                    <NuxtLink to="/">=</NuxtLink>
                    <NuxtLink to="/">Home</NuxtLink>
                    <NuxtLink to="/latest-news">Latest News</NuxtLink>
                    <NuxtLink to="/reviews">Reviews</NuxtLink>
                </div>
                <div>
                    <NuxtLink to="/contact">Contact Us</NuxtLink>
                </div>
            </nav>
        </header>
        <div>
            <slot></slot>
        </div>
    </div>
</template>
<style scoped>
.router-link-exact-active {
    color: #b0695c;
}
</style>