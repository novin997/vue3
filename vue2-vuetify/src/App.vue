<template>
  <v-app>
    <v-toolbar color="purple darken-4" max-height="64px"> 
      <v-toolbar-title class="white--text">HelloEveryNyan</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-item>
        <v-btn class="ma-2" to="/" exact>Home</v-btn>
      </v-toolbar-item>
      <v-toolbar-item>
        <v-btn class="ma-2" to="/animelist" exact>AnimeList</v-btn>
      </v-toolbar-item>
    </v-toolbar>
  <router-view />
  </v-app>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "App",

  components: {
  },

  data: () => ({
    //
  })
});
</script>
