<template>
    <div class="container">
        <div 
            class="colorButton" 
            :style="{ backgroundColor: 'blue' }" 
            @click="$emit('color-change', 'blue')"
        ></div>
        <div
            class="colorButton"
            :style="{ backgroundColor: '#ff0000' }"
            @click="$emit('color-change', '#ff0000')"
        ></div>
        <div
            class="colorButton"
            :style="{ backgroundColor: '#2ae815' }"
            @click="$emit('color-change', '#2ae815')"
        ></div>
        <div 
            class="colorButton" 
            :style="{ backgroundColor: 'yellow' }" 
            @click="$emit('color-change', 'yellow')"
        ></div>
        <div
            class="colorButton"
            :style="{ backgroundColor: 'fuchsia' }"
            @click="$emit('color-change', 'fuchsia')"
        ></div>
    </div>
</template>

<script>
    export default {
        name: 'ColorPresets',
    }
</script>

<style scoped>
    .container {
        border-radius: 10px;
        display: grid;
        background-color: rgb(0, 0, 0, 0.6);
        width: auto;
        height: auto;
        grid-template-columns: repeat(5, 1fr);
        height: 80px;
    }
    .colorButton {
        width: 45px;
        height: 45px;
        margin: auto;
        border-radius: 50%;
    }
    .colorButton:hover {
        border: 3px solid white;
        box-shadow: 0 0 10px #9ecaed;
        transition: 0.25s;
    }
    @media only screen and (max-width: 375px) {
        .container {
            width: 60%;
            margin: auto;
        }
        .colorButton {
            width: 34px;
            height: 35px;
            margin: auto;
            border-radius: 50%;
        }
    }
</style>
