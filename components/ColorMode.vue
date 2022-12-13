<template>
    <div>
        <input type="checkbox" @click="handleClick" />
    </div>
</template>

<script setup>
const colorMode = useColorMode()
let darkMode = false
function handleClick() {
    if(darkMode === false){
        colorMode.value = 'dark'
        darkMode = true;
    }
    else{
        colorMode.value = 'system'
        darkMode= false
    }
    
    
}
</script>

<style >
body {
    background-color: #f9f4ed;
}

.dark-mode body {
    background-color: #2a2a2a;
    color: #eaeaea;
}
input[type="checkbox"] {
    -webkit-appearance: none;
    background-color: white;
    -moz-appearance: none;
    appearance: none;
    position: relative;
    width: 2rem;
    height: 1rem;
    outline: none;
    border: none;
    border-radius: 5rem;
}

input:checked[type="checkbox"] {
    background-color: #2a2a2a;
}

input[type="checkbox"]::before {
    content: " ";
    position: absolute;
    width: calc(1rem * 0.75);
    height: calc(1rem * 0.75);
    background-color: rgb(0, 0, 0);
    border-radius: 5rem;
    top: calc(1rem * 0.13);
    left: 0.2rem;
    transition: 0.2s;
}

input:checked[type="checkbox"]::before {
    left: 1rem;
    background-color: white;
}

.checkboxText {
    font-family: 'Roboto', sans-serif;
    font-size: 30px;
    margin-left: 15px;
}
body {
    background-color: #f9f4ed;
}

.dark-mode body {
    background-color: #2a2a2a;
    color: #eaeaea;
}
</style>
