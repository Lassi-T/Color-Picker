<template>
    <div class="container">
        <div class="colorButton">
            <img class="colorWheelImg" src="../assets/colorWheel.png" alt="color wheel"/>
            <input type="color" v-on:input="$emit('color-change', $event.target.value)"/>
        </div>
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
    import colorWheelImg from '../assets/colorWheel.png'

    export default {
        name: 'ColorPresets',
        data() {
            return {
                colorWheelImg,
            }
        },
    }
</script>

<style scoped>
    input {
        opacity: 0;
        position: absolute;
        top: 0;
        left: 0;    
        width: 100%;
        height: 100%;
    }
    .container {
        border-radius: 10px;
        display: grid;
        background-color: rgb(0, 0, 0, 0.75);
        width: auto;
        height: auto;
        grid-template-columns: repeat(6, 1fr);
        height: 80px;
    }
    .colorWheelImg {
        max-width: 100%;
        max-height: 100%;
    }
    .colorButton {
        position: relative;
        width: 45px;
        height: 45px;
        margin: auto;
        border-radius: 50%;
        transition: 0.15s;
    }
    .colorButton:hover {
        border: 3px solid white;
        box-shadow: 0 0 10px #9ecaed;
    }
    @media only screen and (max-width: 380px) {
        .container {
            width: 90%;
            margin: auto;
        }
        .colorButton {
            width: 30px;
            height: 30px;
            margin: auto;
            border-radius: 50%;
        }
    }
</style>
