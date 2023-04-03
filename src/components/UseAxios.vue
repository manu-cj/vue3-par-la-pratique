<template>
  <div v-for="user in users" :key="user">
    <img :src="user.picture.medium" alt="">
    <p>{{user.name.first}} {{user.name.last}}</p>
    <p>{{user.email}}</p>
    <p>{{user.cell}}</p>
  </div>
  <br><br>
</template>

<script>
import axios from 'axios';
export default {
  name: "UseAxios",
  data(){
    return {
      users : [],
    }
  },
  methods: {

  },
  created() {
    axios.get('https://randomuser.me/api/?results=10').then( response => {
      console.log(response.data.results);
      this.users = response.data.results
    })
  },
}
</script>

<style scoped>

</style>