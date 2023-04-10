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
  style="color: #00d58a"> Est en train d'écrire ...
  </p>
  <br><br>
  <div id="projects">
    <div class="project" v-for="project in projects" :key="project"
         style="width: 33%; height: 500px; background-size: cover"

    >
      <img :src="project.img" alt="" style="width: 100%; height: 100%">
      <div>Date : {{project.date}}</div>
    </div>
  </div>

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
      projects : [
        {
          date : '12/21',
          img : 'src/assets/picture_project/appBudget.png',
        },
        {
          date : '12/21',
          img : 'src/assets/picture_project/wos.png',
        },
        {
          date : '12/21',
          img : 'src/assets/picture_project/appBudget.png',
        },
      ]
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
#projects {
  width: 100%;
  height: 500px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.project {
  border: solid 2px teal;

}

.project:hover {
  border: #d55200 ridge 3px;
  cursor: pointer;
}

.project img {
  z-index: 0;
}
</style>