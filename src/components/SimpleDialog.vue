<template>
    <div class ="dialog-parent">
      <transition :duration ="200">
        <div class="dialog-backdrop" v-show="visible"></div>
      </transition>

      <transition :duration ="1">
        <div class="dialog-window" v-show="visible">
            <header>
                <h1> {{ titre }} </h1>
            </header>
          <div>
            <legend>{{ alt }}</legend>
          </div>

            <div class="main">
               <slot> Valeur par defaut </slot>
            </div>
            <footer>
                <button @click=" visible = false">Close</button>

            </footer>
        </div>
        </transition>
    </div>
</template>

<script>


    export default {
        name: 'SimpleDialog',
      data() {
        return{
          visible: this.initialVisible,
        }

      },
        props: {
            initialVisible: {
                type: Boolean,
                default: false
            },

      titre: {
          type: String,
          default: "le titre par defaut",
      },
          alt: {
            type: String,
            default: "legende par defaut",
          },

     },
    methods: {
            show() {
                this.visible = true;

                /**
                const dest = this.$refs.dialogWindow;
                if (des.animate){
                  this.$nextTick(() => {
                    const first = from.getBoundingClientRect();
                    const last = dest.getBoundingClientRect();
                  });
                }
                 */
     },
    },
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