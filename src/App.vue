<template>
  <div id="app">
    <button>Open</button>

    <SimpleDialog ref="dialog"/>
  </div>
</template>

<script>
import SimpleDialog from "@/components/SimpleDialog";

export default {
  name: 'App',
  components: {
    SimpleDialog

  },
  data: function (){
    return {

    }
  }
}
</script>

<style>

</style>
