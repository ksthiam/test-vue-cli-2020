<template>
  <div id="app">
    <h1>Bonjour</h1>
    <light-box :images-data="imagesDataFiltres" />
  </div>
</template>

<script>
import LightBox from "@/components/LightBox";

export default {
  name: 'App',
  components: {LightBox},
  data() {
    return {
      filtreType: "domestique",
      ListeImages: [

        {
          "src": "images/thumbnails/animals-1.jpeg",
          "dataFullImg": "images/animals-1.jpeg",
          "title":"Gorille",
          "alt":"une jolie image",
          "type": "sauvage"

        },
        {
          "src": "images/thumbnails/animals-2.jpeg",
          "dataFullImg": "images/animals-2.jpeg",
          "title":"banbi",
          "alt":"une jolie image",
          "type": "sauvage"

        },
        {
          "src": "images/thumbnails/animals-3.jpeg",
          "dataFullImg": "images/animals-3.jpeg",
          "title":"cochon",
          "alt":"une jolie image",
          "type": "domestique"
        },
        {
          "src": "images/thumbnails/animals-4.jpeg",
          "dataFullImg": "images/animals-4.jpeg",
          "title":"Rhinocéroce",
          "alt":"une jolie image",
          "type": "sauvage"
        },
        {
          "src": "images/thumbnails/animals-5.jpeg",
          "dataFullImg": "images/animals-5.jpeg",
          "title":"Chat",
          "alt":"une jolie image",
          "type": "domestique"
        },
        {
          "src": "images/thumbnails/animals-6.jpeg",
          "dataFullImg": "images/animals-6.jpeg",
          "title":"Chien",
          "alt":"une jolie image",
          "type": "domestique"
        },
        {
          "src": "images/thumbnails/animals-7.jpeg",
          "dataFullImg": "images/animals-7.jpeg",
          "title":"Guepard",
          "alt":"une jolie image",
          "type": "sauvage",

        },
        {
          "src": "images/thumbnails/animals-8.jpeg",
          "dataFullImg": "images/animals-8.jpeg",
          "title":"Ziraff",
          "alt":"une jolie image",
          "type": "sauvage"
        },
        {
          "src": "images/thumbnails/animals-9.jpeg",
          "dataFullImg": "images/animals-9.jpeg",
          "title":"Chien",
          "alt":"une jolie image",
          "type": "domestique"
        }
      ]
    }
  },
  computed: {
   imagesDataFiltres() {
      return this.ListeImages.filter(({type})=>type===this.filtreType);



    }
  },

}
</script>

<style>

</style>
