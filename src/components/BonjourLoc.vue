<template>
  <div>{{total}}</div>

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

  methods: {

  }

}
</script>

<style scoped>

</style>