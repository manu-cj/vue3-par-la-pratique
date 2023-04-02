<template>
  <div id="textStyle">
    <p>Choisir la couleur
      <select v-model="couleur">
        <option value="white" selected>white</option>
        <option value="red">red</option>
        <option value="green">green</option>
        <option value="pink">pink</option>
      </select>
      taille
      <select v-model="taille">
        <option value="16px" selected>16px</option>
        <option value="20px">20px</option>
        <option value="26px">26px</option>
        <option value="32px">32px</option>
      </select>
    </p>
    <div v-bind:style="{color : couleur, fontSize : taille}">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad consequuntur cumque ex facere, fugit mollitia nisi
      possimus praesentium voluptatum. Deleniti dolor, eius explicabo hic libero nisi nulla perferendis quia voluptatem?
    </div>
  </div>
  <br><br><br>

  <div id="elementCheck">
    <p>Quels langage connaissez-vous ?</p>
    <input type="text" v-model="text">
    <input type="button" @click="addLangage" value="ajouter">
    <div v-for="langage in langages" :key="langage">
      <input type="checkbox" v-model="langage.etat">
      {{langage.lang}}
      <span v-if="langage.etat"> est coché</span>
      <span v-else>est décoché</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "PartTwo",
  data() {
    return {
      couleur: 'white',
      taille: '16px',

      langages : [],
      text : '',
    }
  },

  methods : {
    addLangage() {
      this.langages.push({lang : this.text, etat : false})
    }
  }
}
</script>

<style scoped>

</style>