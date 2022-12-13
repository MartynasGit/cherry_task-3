<template>
    <div>
        <input type="checkbox" @click="handleClick" />
    </div>
</template>

<script setup>
const colorMode = useColorMode()
let colorModeSwitch = true
function handleClick() {

    if (colorModeSwitch) {
        colorMode.preference = 'dark';
        colorModeSwitch = false;
    }
    else {
        colorMode.preference = 'system'
        colorModeSwitch = true;
    }
}
</script>

<style >
input[type="checkbox"] {
    -webkit-appearance: none;
    background-color: rgb(0, 0, 0);
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
    background-color: #ffffff;
}

input[type="checkbox"]::before {
    content: " ";
    position: absolute;
    width: calc(1rem * 0.75);
    height: calc(1rem * 0.75);
    background-color: rgb(255, 255, 255);
    border-radius: 5rem;
    top: calc(1rem * 0.125);
    left: 0.2rem;
    transition: 0.2s;
}

input:checked[type="checkbox"]::before {
    left: 1rem;
    background-color: rgb(0, 0, 0);
}

.checkboxText {
    font-family: 'Roboto', sans-serif;
    font-size: 30px;
    margin-left: 15px;
}
</style>
