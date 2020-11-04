<template>
    <div id="app">


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
            initialVisible:{
                type: Boolean,
                default: false,
            }
    },

        data: function () {
            return{
                visible:this.initialVisible,
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
