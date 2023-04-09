<template>
  <div><h2>{{titre}}</h2><p><slot name="texte"></slot></p>\
    <p><slot name="default"></slot></p>\
  </div>
</template>

<script>
export default {
  name: "TestSlots",
  data() {
    return {

    }
  },

  props : ['titre']

}
</script>

<style scoped>

</style>