<template>
  <v-app>
    <Sidebar :drawer.sync="drawer" />
    <v-app-bar app dark color="primary">
      <v-btn icon @click.stop="toggleDrawer">
        <v-icon>{{ drawer ? 'mdi-chevron-left' : 'mdi-chevron-right' }}</v-icon>
      </v-btn>
      <v-toolbar-title>NG Juarez</v-toolbar-title>
    </v-app-bar>
    <v-main>
      <v-container fluid>
        <!-- Contenido principal de tu aplicación -->
        <router-view></router-view>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Sidebar from "@/components/SideBar.vue";

export default {
  data() {
    return {
      drawer: true,
    };
  },
  components: {
    Sidebar,
  },
  methods: {
    toggleDrawer() {
      this.drawer = !this.drawer;
    },
  },
};
</script>
