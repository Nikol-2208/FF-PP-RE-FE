<template>
  <app>
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
              to="/NewPassword"
          >CAMBIAR CONTRASEÑA</v-btn>
        </v-container>
      </v-form>
    </v-card>
    <v-card
        class="mx-auto my-2"
        max-width="400"
        elevation="0"
    >
      <v-card-title class="text-h4 mb-2">
        Subscripción
      </v-card-title>
      <v-card
          color="rgba(96, 125, 139, 1), rgba(43, 49, 65, 1)"
          gradient="to top right, rgba(43, 49, 65, 0.9), rgba(96, 125, 139, 0.9)">
        <v-card-text class="white--text">Plan: Freemium</v-card-text>
        <v-card-title class="white--text">Gratis</v-card-title>
        <v-card-text class="white--text">Accede a la información sobre presidentes, partidos políticos y candidatos</v-card-text>
      </v-card>
      <v-card-actions class="d-flex justify-center mb-2">
        <v-btn
            block
            outlined
            elevation="1"
            height="50"
            class="d-flex justify-center"
            to="/plan"
        >CAMBIAR A PREMIUM</v-btn>
      </v-card-actions>
    </v-card>
  </app>
</template>

<script>
export default {
  name: "Password",
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