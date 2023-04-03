<template>
<div>
  <h1>Hello world</h1>
  <button @click="disBonjour"> Clic here stranger</button>
</div>
</template>

<script>
export default {
  name: "SayHello",
  data() {
    return {

    }
  },
  props : ['number'],

  methods: {
    disBonjour() {
      document.querySelector('h1').innerHTML = 'Le parent dit bonjour étranger haha'
    }
  }
}

</script>

<style scoped>

</style>