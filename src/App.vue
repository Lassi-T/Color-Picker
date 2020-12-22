<template>
    <div id="app" :style="color" >
        <h1>Colorpicker</h1>
    </div>
</template>

<script>
    export default {
        name: 'App',
        components: {},
        data() {
            return {
                currentColor: '#e309ca',
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
        font-family: Lato;
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
    }
</style>
