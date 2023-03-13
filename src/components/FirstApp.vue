<template>
  <div>
    <p>Date fr :</p> {{dateFr}}<br><br>

    <p>Date  Us:</p> {{dateUs}}<br><br>

  </div>
</template>

<script>
export default {
  name: "FirstApp",

      data() {
        return {
          d: new Date(),
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