<template>
    <div>
      <h1>Usuarios</h1>
  
      <!-- Formulario de Usuario -->
      <v-form @submit.prevent="submitForm">
        <v-container>
          <v-row>
            <v-col cols="12" md="6">
              <v-text-field v-model="nombre" label="Nombre" required></v-text-field>
            </v-col>
  
            <v-col cols="12" md="6">
              <v-text-field v-model="apellido" label="Apellido" required></v-text-field>
            </v-col>
  
            <v-col cols="12" md="6">
              <v-text-field v-model="rol" label="Rol" required></v-text-field>
            </v-col>
  
            <v-col cols="12" md="6">
              <v-text-field v-model="numeroReloj" label="Numero" required></v-text-field>
            </v-col>
  
            <v-col cols="12">
              <v-text-field v-model="correo" label="Correo" required></v-text-field>
            </v-col>
  
            <v-col cols="12">
              <v-btn type="submit" color="primary">Guardar Usuario</v-btn>
            </v-col>
          </v-row>
        </v-container>
      </v-form>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        nombre: "",
        apellido: "",
        rol: "",
        numeroReloj: "",
        correo: "",
      };
    },
    methods: {
      submitForm() {
        // Aquí puedes manejar la lógica para guardar los datos del usuario.
        console.log("Datos del usuario:", {
          nombre: this.nombre,
          apellido: this.apellido,
          rol: this.rol,
          numeroReloj: this.numeroReloj,
          correo: this.correo,
        });
  
        // Puedes enviar estos datos a tu servidor, almacenar en una base de datos, etc.
        // Reinicia los campos del formulario después de guardar.
        this.nombre = "";
        this.apellido = "";
        this.rol = "";
        this.numeroReloj = "";
        this.correo = "";
      },
    },
  };
  </script>
  