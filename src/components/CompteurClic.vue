<template>

<button @click="ajouteUn()">{{valeur}}</button>
</template>

<script>
export default {
  name: "CompteurClic",
  data() {
    return {
      total : 0,
      valeur: 0,
    }
  },
  methods: {
    ajouteUn() {
      this.valeur++;
      this.$emit('incremente');
    }
  }
}
</script>

<style scoped>

</style>