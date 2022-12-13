<template>
    <div>
        <header>
            <nav>
                <div>
                    <NuxtLink to="/">=</NuxtLink>
                    <ul>
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