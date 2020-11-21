<template>
  <div classe="light-box">

    <button @click="$refs.dialog.show ()">open</button>

    <SimpleDialog ref="dialog"
                  titre="Le nouveau titre depuis le parent" >
      Le contenu passe par le parent
    </SimpleDialog>
  </div>
</template>

<script>
import SimpleDialog from "@/components/SimpleDialog";

export default {
  name: 'LightBox',
  components: {
    SimpleDialog

  },
}

</script>

<style>

</style>
