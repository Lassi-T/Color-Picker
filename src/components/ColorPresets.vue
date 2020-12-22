<template>
    <div class="container">
        <div class="wrapper">
            <div class='colorButton' :style="{backgroundColor: 'blue'}"></div>
            <div class='colorButton' :style="{backgroundColor: 'red'}"></div>
            <div class='colorButton' :style="{backgroundColor: 'green'}"></div>
            <div class='colorButton' :style="{backgroundColor: 'yellow'}"></div>
            <div class='colorButton' :style="{backgroundColor: 'purple'}"></div>
        </div>
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
        background-color: rgb(0, 0, 0, 0.6);
        width: auto;
        height: auto;
    }
    .wrapper {
        display: grid;
        grid-template-columns: repeat(5, 1fr);
        height: 75px;
    }
    .colorButton {
        width: 40%;
        height: 70%;
        margin: auto;
        border-radius: 50%;
    }
    .colorButton:hover {
        border: 3px solid white;
        box-shadow: 0 0 10px #9ecaed;
        transition: 0.5s;
    }
</style>
