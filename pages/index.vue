<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card>
        <v-card-title class="headline">
          GitHub API Integration&nbsp;<small class="grey darken-3 rounded-pill px-2"> Client Developed With NuxtJS And Vuetify </small>
        </v-card-title>
        <v-card-text>
          
        </v-card-text>
        <v-card-actions>
          <!-- Turns Off the default "PREFETCH" -->
	        <NuxtLink to="/about" no-prefetch>About page not pre-fetched</NuxtLink>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data () {
    return {
      formData: {}
    }
  },
  head () {
    return {
      title: 'API Integration'
    }
  },
  created () {
    console.log('Do something when page is created')
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
