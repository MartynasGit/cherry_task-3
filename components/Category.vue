<template>
    <div>
        <button class="categoryBtn">{{ category }}</button>
    </div>
</template>

<script setup>
const { category } = defineProps(['category'])
</script>

<style scoped>
.categoryBtn {
    border: 2px solid #2a2a2a;
    border-radius: 22px;
    padding: 3px 10px;
    margin: 0 1px;
    transition: ease-in-out 0.3s;
}

.categoryBtn:focus {
    color: #af695c;
    border-color: #af695c;
}

.categoryBtn:hover {
    transform: scale(1.08);
}
.dark-mode .categoryBtn:focus {
    color: #af695c;
    border-color: #af695c;
}

.dark-mode .categoryBtn:hover {
    transform: scale(1.08);
}

.dark-mode .categoryBtn {
    color: var(--color-light);
    border-color: var(--color-light);
}
</style>