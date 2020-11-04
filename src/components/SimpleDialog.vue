<template>
    <div class ="dialog-parent">

        <div class="dialog-backdrop" v-show="visible"></div>
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

<style scoped>
    .dialog-window {
        position: relative;
        pointer-events: auto;
    }
    .dialog-parent {
        pointer-events: none;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .dialog-parent,
    .dialog-backdrop {
        position: fixed;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
    }
    .dialog-backdrop {
        pointer-events: auto;
        background-color: rgba(255, 30, 80, 0.5);
    }

</style>