<script>
// import FirstApp from "./components/FirstApp.vue";
// import PartTwo from "./components/PartTwo.vue";
// import SayHello from "./components/SayHello.vue";

// import CompteurClic from "./components/CompteurClic.vue";
// import BonjourLoc from "./components/BonjourLoc.vue";
// import UseAxios from "./components/UseAxios.vue";
// import TestSlots from "./components/TestSlots.vue";
import ListeEmployer from "./components/ListeEmployer.vue";

export default {
  name: 'App',
  data(){
    return {
      total : 0,
    }
  },

  methods: {
    // plusUn() {
    //   this.total++
    // }
  },

  components: {
    // CompteurClic,
    // UseAxios,
    // BonjourLoc,
    // TestSlots,
    ListeEmployer,
  },
}

</script>

<template id="app">
      <!--      <FirstApp/>-->
      <!--    <part-two/>-->
<!--      <SayHello ></SayHello>-->
<!--      <BonjourLoc number="10" ></BonjourLoc>-->
<!--      <BonjourLoc number="100" ></BonjourLoc>-->
<!--      <BonjourLoc number="1000" ></BonjourLoc>-->
<!--   {{total}}-->
<!--      <br><br>-->
<!--      <CompteurClic @incremente="plusUn"></CompteurClic>-->
<!--      <CompteurClic @incremente="plusUn"></CompteurClic>-->
<!--      <CompteurClic @incremente="plusUn"></CompteurClic>-->
<!--      <UseAxios/>-->

<!--      <TestSlots titre="Titre de l'article o">-->
<!--        <template v-slot:texte>-->
<!--          <p>Texte de l'article</p>-->
<!--        </template>-->
<!--        <p>Ce texte est intégré dans le slot default</p>-->
<!--      </TestSlots>-->
      <ListeEmployer>
        <template v-slot="slotProps">
          <span><em>{{slotProps.personne.prenom}}</em></span>&nbsp;
          <span><strong>{{slotProps.personne.nom.toUpperCase()}}</strong></span>
        </template>
      </ListeEmployer>
</template>

<style>
#app {
  width: 100%;
  height: 100%;
}
</style>
