<template>
  <div>{{nombre}}</div>

</template>

<script>
export default {
  name: "BonjourLoc",
  data() {
    return {
      nbrClics : 0,
      nombre : Math.floor(Math.random() * this.number +1)
    }
  },
  props : ['number'],

}
</script>

<style scoped>

</style>