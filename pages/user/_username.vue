<template>
  <v-container>
    <h1>Dinamic Page For Users</h1>
  </v-container>
</template>

<script lang="ts">
import Vue from 'vue'
import UserDetails from '../../models/UserDetails'

export default Vue.extend({

  // The asyncData hook and fetch hook should return a promise using return or implicity with async/await
  async asyncData({ params, $axios, error }) {
    await $axios.get(`https://api.github.com/users/${params.username}`).then(response => {
      console.log(response)
    }).catch((e) => console.log(e))
  },
  data () {
    return {
      userDetails: {} as UserDetails
    }
  },
  head () {
    return {
      title: 'User Details'
    }
  },
  methods: {
    clickHandler () {
      alert('Clicked!')
    }
  }
})
</script>

<style scoped>

</style>