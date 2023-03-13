<template>
  <div>
    <p>Date fr :</p> {{dateFr}}<br><br>

    <p>Date  Us:</p> {{dateUs}}<br><br>

    <div v-bind:id="id">
      <p v-text="textBrut"></p>
      <p v-html="textHtml"></p>
    </div>

  </div>
</template>

<script>
export default {
  name: "FirstApp",

      data() {
        return {
          d: new Date(),
          url : "../assets/logo.svg",
          id : "vue",
          textBrut : "simple text",
          textHtml : "<font color ='red'><u>Un texte rouge souligné</u></font>"
        }
      },
  computed: {
    dateFr() {
      return this.d.toLocaleTimeString();
    },

    dateUs() {
      return this.d.toLocaleTimeString('en-US')
    }
  }
}
</script>

<style scoped>

</style>