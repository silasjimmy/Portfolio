<template>
  <v-app>
    <v-app-bar app elevate-on-scroll color="primary" dark>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-toolbar-title> Silas Jimmy </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn link plain to="/about" class="text-none">About</v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",
  title: "Silas Jimmy",
};
</script>
