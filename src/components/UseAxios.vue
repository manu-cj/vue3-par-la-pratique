<template>
  <table v-for="user in users" :key="user">
    <tr>
      <td>
        <img :src="user.picture.large" alt="">
      </td>
      <td>
        {{ user.name.first }} {{ user.name.last }}
        <br>
        {{ user.email }}
        <br>
        {{ user.cell }}
      </td>
    </tr>
  </table>
  <br><br>
</template>

<script>
import axios from 'axios';

export default {
  name: "UseAxios",
  data() {
    return {
      users: [],
    }
  },
  methods: {},
  created() {
    axios.get('https://randomuser.me/api/?results=10').then(response => {
      console.log(response.data.results);
      this.users = response.data.results
    })
  },
}
</script>

<style scoped>

</style>