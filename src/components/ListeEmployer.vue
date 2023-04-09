<template>
<!--  <div v-for="personne in personnes" :key="personne">-->
<!--      <slot :personne="personne"></slot>-->
<!--  </div>-->
<!--  <div>-->
<!--    <p v-if="compteur < 9">{{texte="Le compteur est de : "}}{{compteur}}</p>-->
<!--    <p v-else>{{texte="Stop tu va revenir à 0"}}</p>-->
<!--    <button @click="compteur++">Incrémenter</button>-->
<!--  </div>-->
  <input type="text" v-model="msg">
  <p v-show="affiche"
  style="color: #00d58a"> Est entrain d'écrire ...
  </p>
</template>

<script>
export default {
  name: "ListeEmployer",
  data() {
    return {
      personnes: [
        {
          prenom: 'Jean',
          nom: 'Segur',
        },
        {
          prenom: 'Pierre',
          nom: 'Dumanier',
        }

      ],
      compteur : 0,
      texte : '',
      msg : '',
      affiche : false,
      t : null,
    }
  },

  watch : {
    compteur(valeur) {
      if (valeur===10) {
        this.compteur =0;
      }
    },

    msg() {
      if (this.affiche) {
        clearTimeout(this.t);
      }
      this.affiche = true;
      this.t = setTimeout( ()=> {
        this.affiche = false
      }, 3000)
    }
  }
}

</script>

<style scoped>

</style>