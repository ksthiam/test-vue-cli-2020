<template>
  <div class="light-box">
    <ul>
      <li v-for="{src, dataFullImg} in imagesData" :key="src">
        <img :src="src" @click="afficheImg(dataFullImg)" alt=""/>
      </li>
    </ul>

    <SimpleDialog ref="dialog"
                  titre="Le titre de cette instance">
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
  components: {
    SimpleDialog

  },
  data() {
    return {
      imageCourante: "",
      imagesData:[],

    }
  },
  created() {
    fetch("images-data.json")
    .then(rep=> rep.json())
    .then(json=> this.imagesData = json);
  },
  methods: {
    afficheImg(url) {
    this.imageCourante = url;
    this.$refs.dialog.show();

      //affichImage() {
       //this.$refs.dialo.show();
       //this.imageCourante='images/animals-1.jpeg'


  }
  },
  }
  


</script>