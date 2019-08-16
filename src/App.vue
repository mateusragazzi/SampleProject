<template>
  <v-app>
    <v-toolbar>
      <v-toolbar-title>Sample Project</v-toolbar-title>
      <v-spacer></v-spacer>
      <router-link class="menu-link" to="/">Home</router-link>
      <router-link class="menu-link" to="/about">About us</router-link>
    </v-toolbar>
    <v-container fill-height text-center>
      <v-fade-transition mode="out-in">
        <router-view></router-view>
      </v-fade-transition>
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

.container,
.v-application--wrap {
  background: white;
}

.v-toolbar__content {
  background: #000a12;
  color: white;
}
.menu-link {
  margin-right: 15px;
  color: white !important;
  text-decoration: none;
}
</style>
