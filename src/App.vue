<template>
  <v-app>
    <nav class="container mx-auto py-4">
      <v-toolbar app flat color="white">
        <v-toolbar-side-icon
          @click.stop="drawer = !drawer"
          class="hidden-md-and-up"
        ></v-toolbar-side-icon>

        <v-toolbar-title class="headline">
          <v-avatar color="surface-variant" size="50px">
            <span class="text-h5">HT</span>
          </v-avatar>
          Huy Ta</v-toolbar-title
        >

        <v-spacer></v-spacer>

        <v-toolbar-items class="hidden-sm-and-down">
          <v-btn flat to="/">About me</v-btn>
          <v-btn flat to="/resumse">Resume</v-btn>
          <v-btn flat to="/contact">Contact</v-btn>
        </v-toolbar-items>
      </v-toolbar>
    </nav>

    <v-content class="container mx-auto py-4">
      <!-- Display view pages here based on route -->

      <router-view></router-view>
    </v-content>
    <v-footer class="flex flex-col">
      <v-divider :thickness="4" class="border-opacity-75 w-2/3"></v-divider>
      <div class="flex flex-row container mx-auto pb-6 pt-4 pl-4 gap-x-6">
        <v-icon icon="mdi-twitter" size="x-large" />
        <v-icon icon="mdi-linkedin" size="x-large" />
        <p class="flex-grow text-end font-semibold">{{ new Date().getFullYear() }}</p>
      </div>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  data() {
    return {
      drawer: false // Hide mobile side menu by default
    }
  }
}
</script>
