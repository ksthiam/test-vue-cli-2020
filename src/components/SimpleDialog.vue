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


            </footer>
        </div>
    </div>
</template>

<script>


    export default {
        name: 'SimpleDialog',
        props:{
    },

        data: function () {
            return{
                visible:false,
            }

        },
    methods: {
            show(){
                this.visible= true;
            }
    }

    }
</script>

<style>

</style>
