<template>
    <div id="app">


        <div class="dialog-window" v-show="visible">
            <header>
                <h1>{{titre}}</h1>
            </header>
            <div class="main">
                Contenu
            </div>
            <footer>
                <button @click=" visible = false">Close</button>

            </footer>
        </div>
    </div>
</template>

<script>


    export default {
        name: 'SimpleDialog',
        props:{
            titre:{
                type: String,
                default: "le titre par defaut",
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
