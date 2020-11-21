<template>
  <div class="light-box">
    <ul>
      <li><img @click="$refs.dialog.show()" src="images/thumbnails/animals-1.jpeg" data-full-img="images/animals-1.jpeg" alt=""/></li>
      <li><img @click="$refs.dialog.show()" src="images/thumbnails/animals-2.jpeg" data-full-img="images/animals-2.jpeg" alt=""/></li>
      <li><img @click="$refs.dialog.show()" src="images/thumbnails/animals-3.jpeg" data-full-img="images/animals-3.jpeg" alt=""/></li>
      <li><img @click="$refs.dialog.show()" src="images/thumbnails/animals-4.jpeg" data-full-img="images/animals-4.jpeg" alt=""/></li>
      <li><img @click="$refs.dialog.show()" src="images/thumbnails/animals-5.jpeg" data-full-img="images/animals-5.jpeg" alt=""/></li>
      <li><img @click="$refs.dialog.show()" src="images/thumbnails/animals-6.jpeg" data-full-img="images/animals-6.jpeg" alt=""/></li>
      <li><img @click="$refs.dialog.show()" src="images/thumbnails/animals-7.jpeg" data-full-img="images/animals-7.jpeg" alt=""/></li>
      <li><img @click="$refs.dialog.show()" src="images/thumbnails/animals-8.jpeg" data-full-img="images/animals-8.jpeg" alt=""/></li>
      <li><img @click="$refs.dialog.show()" src="images/thumbnails/animals-9.jpeg" data-full-img="images/animals-9.jpeg" alt=""/></li>
    </ul>

    <button @click="$refs.dialog.show()">Open</button>

    <SimpleDialog ref="dialog"
                  titre="Le titre de cette instance">
      <img src="images/animals-1.jpeg" alt=""
           width="400" height="200">
      <!-- On met la taille pour ne pas avoir à écrire
            un code qui attend le chargement de l'image -->
    </SimpleDialog>

  </div>
</template>