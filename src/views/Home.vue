<template>
  <v-layout align-center justify-center column fill-height>
    <v-flex class="gradient" pa-5 md12 align-center>
      <v-layout align-center justify-center row fill-height>
        <v-flex>
          <h1>Welcome to Sample Project</h1>
        </v-flex>
      </v-layout>
    </v-flex>
    <v-flex pa-5 md12>
      <p>This project was made to save an sample of a project which uses Vue + Vuetify + Cordova to build Android and Web applications. It contains:</p>
      <p v-for="name in tech" :key="name" v-text="name"></p>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      tech: [
        "Vue - 2.6.10 or +",
        "Vuetify - 2.0.0 or +",
        "Vue Router - 3.0.3 or +",
        "Vuex - 3.0.1 or +",
        "Cordova - 2.3.6 or +",
        "Babel - 10.0.1 or +",
        "ESlint - 5.0.0 or +"
      ]
    };
  }
};
</script>

<style>
.container {
  width: 100%;
  margin: 0;
  max-width: none;
  padding: 0;
}
.gradient {
  width: 100%;
  color: white;
  background: radial-gradient(#000a12, #263238);
}
</style>

