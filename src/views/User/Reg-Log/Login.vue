<template>
  <app>
    <v-card
        class="mx-auto my-2"
        max-width="400"
        elevation="0"
    >
      <v-card-title></v-card-title>
      <v-card-title class="text-h4 mb-2">
        Inicia Sesión
      </v-card-title>
      <v-form class="action">
        <v-container fluid>
          <h3 class="font-weight-light">Dirección de correo electrónico</h3>
          <v-text-field
              v-model="email"
              :rules="emailRules"
              label="Dirección de correo electrónico"
              required
              solo
          ></v-text-field>
          <h3 class="font-weight-light">Contraseña</h3>
          <v-text-field
              :append-icon="show2 ? 'mdi-eye' : 'mdi-eye-off'"
              :rules="[rules.required, rules.min]"
              :type="show2 ? 'text' : 'password'"
              name="input-10-2"
              label="Contraseña"
              hint="At least 8 characters"
              value=""
              class="input-group--focused"
              @click:append="show2 = !show2"
              solo
          ></v-text-field>
          <v-btn text color="grey" class="mx-6" to="/password">¿Se te ha olvidado la contraseña?</v-btn>
          <v-btn block color="red" class="white--text" height="50" to="/">INICIAR SESIÓN</v-btn>
        </v-container>
      </v-form>
      <v-divider></v-divider>
      <v-card-actions class="d-flex justify-center mb-2">
        <v-spacer></v-spacer>
        <h4>¿No tienes cuenta?</h4>
        <v-spacer></v-spacer>
      </v-card-actions>
      <v-card-actions class="d-flex justify-center mb-2">
        <v-btn
            block
            outlined
            elevation="1"
            height="50"
            class="d-flex justify-center"
            to="/Register"
        >REGÍSTRATE</v-btn>
      </v-card-actions>
    </v-card>
  </app>
</template>

<script>
export default {
  name: "Login",
  data () {
    return {
      show1: false,
      show2: false,
      password: 'Password',
      rules: {
        required: value => !!value || 'Requerido.',
        min: v => v.length >= 8 || 'Mínimo 8 carácteres',
      },
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