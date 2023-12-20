<template>
    <v-navigation-drawer app dark color="black" :value="drawer" @input="$emit('update:drawer', $event)">
      <v-list>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="text-center">
              <v-img src="@/assets/logo.png" alt="Vue Logo" max-height="70"></v-img>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
  
        <!-- Opción para la vista de Control -->
        <v-list-item to="/control" class="text-center">
          <v-list-item-icon>
            <v-icon>mdi-monitor-dashboard</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>Control</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
  
        <!-- Opción para la vista de Usuarios -->
        <v-list-item to="/usuarios" class="text-center">
          <v-list-item-icon>
            <v-icon>mdi-account-group</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>Usuarios</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </template>
  
  <script>
  export default {
    props: {
      drawer: Boolean,
    },
  };
  </script>
  