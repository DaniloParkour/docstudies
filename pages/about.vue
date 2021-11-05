<template>
  <div>
    <v-row class="ml-4 mt-2">
      <div @click="$router.go(-1)">
        <v-icon>mdi-arrow-left-bold</v-icon>&nbsp;Back
      </div>
    </v-row>
    <v-row>
    <v-col class="text-center">
      <blockquote class="blockquote">
        &#8220;About.&#8221;
        <footer>
          <small>
            <em>&mdash;About</em>
          </small>
        </footer>
      </blockquote>
    </v-col>
  </v-row>
  </div>
</template>
