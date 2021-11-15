<template>
  <v-card
      class="mx-auto my-2"
      max-width="400"
      elevation="0"
  >
    <v-card-title></v-card-title>
    <v-card-title class="text-h4 mb-2">
      Cuenta
    </v-card-title>
    <v-form class="action">
      <v-container fluid>
        <h3 class="font-weight-light">Correo electrónico</h3>
        <v-text-field
            v-model="email"
            :rules="emailRules"
            label="Dirección de correo electrónico"
            required
            solo
        ></v-text-field>
        <h3 class="font-weight-light">Contraseña</h3>
        <v-btn
            block
            outlined
            elevation="1"
            height="50"
            class="d-flex justify-center"
        >CAMBIAR CONTRASEÑA</v-btn>
      </v-container>
    </v-form>
    <v-card elevation="0">
      <v-container></v-container>
      <v-container></v-container>
      <v-container></v-container>
      <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn color=#2B3141 class="white--text" width="159" height="39">INGRESAR</v-btn>
        <v-spacer></v-spacer>
      </v-card-actions>
    </v-card>
  </v-card>
</template>

<script>
export default {
  name: "ARegister",
  data () {
    return {
      show1: false,
      show2: false,
      email: '',
      emailRules: [
        v => !!v || 'Email es requerido',
        v => /.+@.+\..+/.test(v) || 'Email debe ser válido',
      ],
    }
  },
}
</script>

<style scoped>

</style>