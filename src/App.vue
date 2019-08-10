<template>
  <v-app>
    <v-toolbar>
      <v-toolbar-title>Sample Project</v-toolbar-title>
      <v-spacer></v-spacer>
      <router-link class="menu-link" to="/">Home</router-link>
      <router-link class="menu-link" to="/about">About us</router-link>
    </v-toolbar>
    <v-container fill-height text-center>
      <v-layout row wrap align-center>
        <v-fade-transition mode="out-in">
          <router-view></router-view>
        </v-fade-transition>
      </v-layout>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    //
  })
};
</script>

<style>
  h1 {
    margin-bottom: 25px;
  }
  .menu-link {
    margin-right: 15px;
  }
</style>
