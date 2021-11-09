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
    console.log('Runing in ' + (process.client  ? 'client' : 'server'))
    await $axios.get(`https://api.github.com/users/${params.username}`).then(response => {
      // console.log(response)
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
  // In beforeMount and in mounted we have access to window that normal window and
  // document access is not directly because vue/nuxt use a node server
  beforeMount () {
    console.log('hello beforeMount. Base URI from document is ' + document.baseURI)
  },
  mounted () {
    console.log('hello mounted. Window is a ' + window)
    if(pro)
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