<template>
  <div id="app">
    <h1>Bonjour</h1>
    <light-box :initial-images-data="ListeImages" />
  </div>
</template>

<script>
import LightBox from "@/components/LightBox";

export default {
  name: 'App',
  components: {LightBox},
  data() {
    return {
      ListeImages: [

        {
          "src": "images/thumbnails/animals-1.jpeg",
          "dataFullImg": "images/animals-1.jpeg",
          "title":"Gorille"
        },
        {
          "src": "images/thumbnails/animals-2.jpeg",
          "dataFullImg": "images/animals-2.jpeg",
          "title":"banbi"

        },
        {
          "src": "images/thumbnails/animals-3.jpeg",
          "dataFullImg": "images/animals-3.jpeg",
          "title":"cochon"
        },
        {
          "src": "images/thumbnails/animals-4.jpeg",
          "dataFullImg": "images/animals-4.jpeg",
          "title":"Rhinocéroce"
        },
        {
          "src": "images/thumbnails/animals-5.jpeg",
          "dataFullImg": "images/animals-5.jpeg",
          "title":"Chat"
        },
        {
          "src": "images/thumbnails/animals-6.jpeg",
          "dataFullImg": "images/animals-6.jpeg",
          "title":"Chien"
        },
        {
          "src": "images/thumbnails/animals-7.jpeg",
          "dataFullImg": "images/animals-7.jpeg",
          "title":"Guepard"
        },
        {
          "src": "images/thumbnails/animals-8.jpeg",
          "dataFullImg": "images/animals-8.jpeg",
          "title":"Ziraff"
        },
        {
          "src": "images/thumbnails/animals-9.jpeg",
          "dataFullImg": "images/animals-9.jpeg",
          "title":"Chien"
        }
      ]
    }
  },

}
</script>

<style>

</style>
