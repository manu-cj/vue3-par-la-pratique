<template>
  <div v-for="personne in personnes" :key="personne">
      <slot :personne="personne"></slot>
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

      ]
    }
  }
}

</script>

<style scoped>

</style>