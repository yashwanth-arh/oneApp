<template>
  <v-app>
    <v-app-bar>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Title</v-toolbar-title>
      <v-spacer></v-spacer>

      <v-btn variant="plain" class="d-none d-md-block">
        <router-link to="/">Home</router-link>
      </v-btn>

      <v-btn variant="plain" class="d-none d-md-block" d-sm-none>
        <router-link to="/about">About</router-link>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-btn variant="plain" class="d-block d-md-none">
        <router-link to="/">Home</router-link>
      </v-btn>

      <v-btn variant="plain" class="d-block d-md-none" d-sm-none>
        <router-link to="/about">About</router-link>
      </v-btn>
    </v-navigation-drawer>

    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    drawer: null,
  }),
};
</script>
