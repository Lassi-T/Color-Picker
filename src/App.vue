<template>
    <div id="app" :style="color">
        <div class='container'>
            <h1>Colorpicker</h1>
            <ColorPresets />
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
                currentColor: '#2b2b2b',
            }
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
        font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
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
        text-overflow: ellipsis;
        margin: auto;
        padding-bottom: 1em;
    }
    .container {
        width: 55%;
        margin: auto;
    }
</style>
