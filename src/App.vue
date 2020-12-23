<template>
    <div id="app" :style="color">
        <div class="container">
            <h1>Color Picker</h1>
            <ColorPresets v-on:color-change="changeColor" />
        </div>
    </div>
</template>

<script>
    import ColorPresets from './components/ColorPresets'

    export default {
        name: 'App',
        components: {
            ColorPresets,
        },
        data() {
            return {
                currentColor: '#2B2C2D',
            }
        },
        methods: {
            changeColor(color) {
                this.currentColor = color
            },
        },
        computed: {
            color() {
                return {
                    '--color': this.currentColor,
                }
            },
        },
    }
</script>

<style>
    #app {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        color: white;
        background-color: var(--color);
        width: 100vw;
        height: 100vh;
        position: absolute;
        left: 0;
        top: 0;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
    }
    h1 {
        font-size: 45px;
        text-overflow: ellipsis;
        margin: auto;
        padding-bottom: 1em;
        text-shadow: 2px 2px black;
    }
    .container {
        width: 80%;
        margin: auto;
    }
    @media only screen and (min-width: 768px) {
        .container {
            width: 70%;
            margin: auto;
        }
    }
    @media only screen and (min-width: 1000px) {
        .container {
            width: 35%;
            margin: auto;
        }
    }
</style>
