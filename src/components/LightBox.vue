<template>
  <div class="light-box">
    <ul>
      <li v-for="{src, dataFullImg, title} in imagesData" :key="src">
        <img @click="afficheImg(dataFullImg,title)"
             :src="src" alt="" :title="title"/>
      </li>
    </ul>

    <SimpleDialog ref="dialog"
           :titre="titreDialog">
      <img :src="imageCourante" alt=""
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
      imagesData: [
      ],
      titreDialog:'',

    }
  },
  props: {
    initialImagesData: {
      type: [String, Array],
      default: "default-images-data.json",
    },
  },
  created() {
    if (typeof this.initialImagesData ==='string') {
      fetch(this.initialImagesData)
          .then(rep => rep.json())
          .then(json => this.imagesData = json);
    } else {
      this.imagesData = this.initialImagesData;
    }

  },
  methods: {
    afficheImg(imageCourante, titreDialog) {
      this.$refs.dialog.show();
      this.titreDialog = titreDialog
      this.imageCourante = imageCourante
    }
  },
}



</script>