<template>
  <v-app dark>
    <v-app-bar app dark>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>VBLab</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn class="ma-2" outlined>
        <v-icon left>mdi-email</v-icon>
        Contact Us
      </v-btn>
    </v-app-bar>

    <v-main>
      <!-- Provides the application the proper gutter -->
      <v-container fluid>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {}
</script>

<style scoped>
v-container{
  padding: 50px;
}
</style>