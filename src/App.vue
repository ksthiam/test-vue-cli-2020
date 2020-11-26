<template>
  <div id="app">
    <h1>Bonjour</h1>
    <button  @click= "filtreType = null ">Tous</button>

    <button  v-for="type of listeFiltre" :key="type"
           @click= "filtreType = type"> {{type}}</button>

    <h2>Les Tri</h2>
    <button  v-for="tri of listeNomTri" :key="tri"
             @click= "nomTri = tri"> {{tri}}</button>





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
      filtreType: null,
      nomTri: 'taille',
      ListeImages: [
        {
          "src": "images/thumbnails/animals-1.jpeg",
          "dataFullImg": "images/animals-1.jpeg",
          "title": "Gorille",
          "type": "sauvage",
          "tris": {
            "taille": 1.4,
            "poids": 80,
            "age": 8
          }

        },
        {
          "src": "images/thumbnails/animals-2.jpeg",
          "dataFullImg": "images/animals-2.jpeg",
          "title": "Banbi",
          "type": "sauvage",
          "tris": {
            "taille": 1.2,
            "poids": 40,
            "age": 8
          }

        },
        {
          "src": "images/thumbnails/animals-3.jpeg",
          "dataFullImg": "images/animals-3.jpeg",
          "title": "Cochon",
          "type": "domestique",
          "tris": {
            "taille": 1,
            "poids": 40,
            "age": 5
          }

        },
        {
          "src": "images/thumbnails/animals-4.jpeg",
          "dataFullImg": "images/animals-4.jpeg",
          "title": "Rhinocéroce",
          "alt": "une jolie image",
          "type": "sauvage",
          "tris": {
            "taille": 1.9,
            "poids": 400,
            "age": 45
          }

        },
        {
          "src": "images/thumbnails/animals-5.jpeg",
          "dataFullImg": "images/animals-5.jpeg",
          "title": "Chat",
          "alt": "une jolie image",
          "type": "domestique",
          "tris": {
            "taille": 0.5,
            "poids": 5,
            "age": 50
          }

        },
        {
          "src": "images/thumbnails/animals-6.jpeg",
          "dataFullImg": "images/animals-6.jpeg",
          "title": "Chien",
          "alt": "une jolie image",
          "type": "domestique",
          "tris": {
            "taille": 1.4,
            "poids": 20,
            "age": 4
          }
        },
        {
          "src": "images/thumbnails/animals-7.jpeg",
          "dataFullImg": "images/animals-7.jpeg",
          "title": "Guépard",
          "alt": "une jolie image",
          "type": "sauvage",
          "tris": {
            "taille": 1.4,
            "poids": 60,
            "age": 6
          }

        },
        {
          "src": "images/thumbnails/animals-8.jpeg",
          "dataFullImg": "images/animals-8.jpeg",
          "title": "Ziraff",
          "alt": "une jolie image",
          "type": "sauvage",
          "tris": {
            "taille": 9,
            "poids": 180,
            "age": 15
          }

        },
        {
          "src": "images/thumbnails/animals-9.jpeg",
          "dataFullImg": "images/animals-9.jpeg",
          "title": "Chien",
          "alt": "une jolie image",
          "type": "domestique",
          "tris": {
            "taille": 1.4,
            "poids": 20,
            "age": 8
          },

        }
      ]
    }
  },
  computed: {
    imagesDataFiltres() {
      let data = [...this.ListeImages]
      if (this.filtreType) {
        data = data.filter(({type}) => type === this.filtreType);
      } if (this.nomTri) {
        data.sort((a,b)=> a.tris[this.nomTri] - b.tris.[this.nomTri])
      }
      return data;
    },
    listeFiltre() {
      return new Set(this.ListeImages.map(obj => obj.type));

  },
  listeNomTri() {

    return Object.keys(this.ListeImages[0].tris);
  },

}
}
</script>

<style scoped>


</style>
