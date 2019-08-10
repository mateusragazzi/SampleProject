<template>
  <div class="home">
    <h1>Welcome to Sample Project</h1>
    <p>This project was made to save an sample of a project which uses Vue + Vuetify + Cordova to build Android and Web applications. It contains:</p>
    <v-list>
      <v-list-item-content v-for="name in tech" :key="name">
        <v-list-item-title>{{name}}</v-list-item-title>
      </v-list-item-content>
    </v-list>
  </div>
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
        "Corodova - 2.3.6 or +",
        "Babel - 10.0.1 or +",
        "ESlint - 5.0.0 or +"
      ]
    };
  }
};
</script>

