<template>
  <div class="light-box">
    <ul>
      <li><img src="images/thumbnails/animals-1.jpeg"  @click="afficheImg('images/animals-1.jpeg')"   alt=""/></li>
      <li><img src="images/thumbnails/animals-1.jpeg"  @click="afficheImg('images/animals-2.jpeg')" alt=""/></li>
      <li><img src="images/thumbnails/animals-1.jpeg"  @click="afficheImg('images/animals-3.jpeg')"   alt=""/></li>
      <li><img src="images/thumbnails/animals-1.jpeg"  @click="afficheImg('images/animals-4.jpeg')"   alt=""/></li>
      <li><img src="images/thumbnails/animals-1.jpeg"  @click="afficheImg('images/animals-5.jpeg')"    alt=""/></li>
      <li><img src="images/thumbnails/animals-1.jpeg"  @click="afficheImg('images/animals-6.jpeg')"    alt=""/></li>
      <li><img src="images/thumbnails/animals-1.jpeg"  @click="afficheImg('images/animals-7.jpeg')"   alt=""/></li>
      <li><img src="images/thumbnails/animals-1.jpeg"  @click="afficheImg('images/animals-8.jpeg')"    alt=""/></li>
      <li><img src="images/thumbnails/animals-1.jpeg"  @click="afficheImg('images/animals-9.jpeg')"  alt=""/></li>
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
      imageCourante: [
        {
          "src": "images/thumbnails/animals-1.jpeg",
          "dataFullImg": "images/animals-1.jpeg"
        },
        {
          "src": "images/thumbnails/animals-2.jpeg",
          "dataFullImg": "images/animals-2.jpeg"
        },
        {
          "src": "images/thumbnails/animals-3.jpeg",
          "dataFullImg": "images/animals-3.jpeg"
        },
        {
          "src": "images/thumbnails/animals-4.jpeg",
          "dataFullImg": "images/animals-4.jpeg"
        },
        {
          "src": "images/thumbnails/animals-5.jpeg",
          "dataFullImg": "images/animals-5.jpeg"
        },
        {
          "src": "images/thumbnails/animals-6.jpeg",
          "dataFullImg": "images/animals-6.jpeg"
        },
        {
          "src": "images/thumbnails/animals-7.jpeg",
          "dataFullImg": "images/animals-7.jpeg"
        },
        {
          "src": "images/thumbnails/animals-8.jpeg",
          "dataFullImg": "images/animals-8.jpeg"
        },
        {
          "src": "images/thumbnails/animals-9.jpeg",
          "dataFullImg": "images/animals-9.jpeg"
        }
      ]

    }
  },
  methods: {
    afficheImg(url) {
      this.imageCourante=url;
      this.$refs.dialo.show();

      //affichImaage() {
       // this.$refs.dialo.show();
       // this.imageCourante='images/animals-1.jpeg'

    }
  },
  
}

</script>