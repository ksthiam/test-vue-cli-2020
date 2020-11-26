<template>
  <div class="light-box">
    <transition-group name="list" tag="ul">
      <li v-for="{src, dataFullImg, title, alt} in imagesData" :key="src">
        <img @click="afficheImg(dataFullImg,title, alt, $event.target)"
             :src="src" :alt="alt" :title="title"/>
      </li>
    </transition-group>

    <SimpleDialog ref="dialog"
           :titre="titreDialog" :alt="altDialog">

      <img rel="desAnim" :src="imageCourante"
           width="400" height="200">
      <!-- On met la taille pour ne pas avoir à écrire
            un code qui attend le chargement de l'image -->
    </SimpleDialog>
  </div>
</template>

<script>
import SimpleDialog from "@/components/SimpleDialog";

export default {
  name: 'LightBox',
  components: {SimpleDialog},
  data() {
    return {
      imageCourante: "images/animals-1.jpeg",
      titreDialog:"",
      altDialog: "",


    }

  },
  props: {
    imagesData: {
      type: Array,

    },
  },

  methods: {
    afficheImg(imageCourante , titredeDialog,lealtDialog) {
      this.$refs.dialog.show();
      this.titreDialog = titredeDialog
      this.altDialog = lealtDialog
      this.imageCourante = imageCourante
    }
  },
}



</script>
<style class="scoped">


</style>