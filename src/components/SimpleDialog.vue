<template>
    <div id="app">
        <button>Open</button>

        <div class="dialog-window" v-show="visible">
            <header>
                <h1>Le titre</h1>
            </header>
            <div class="main">
                Contenu
            </div>
            <footer>
                <button @click="visible = false">Close</button>
            </footer>
        </div>
    </div>
</template>

<script>


    export default {
        name: 'SimpleDialog',
        props: {
        visible: {}

        }
    }
</script>

<style>

</style>
