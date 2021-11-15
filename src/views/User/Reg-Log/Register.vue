<template>
  <app>
    <v-card
        class="mx-auto my-2"
        max-width="400"
        elevation="0"
    >
      <v-card-title></v-card-title>
      <v-card-title class="text-h4 mb-2">
        Regístrate
      </v-card-title>
      <v-form class="action">
        <v-container fluid>
          <h3 class="font-weight-light">¿Cuál es tu nombre?</h3>
          <v-text-field
              v-model="name"
              :rules="nameRules"
              label="Introduce tu nombre"
              required
              solo
          ></v-text-field>
          <h3 class="font-weight-light">¿Cuáles son tus apellidos?</h3>
          <v-text-field
              v-model="lastname"
              :rules="lastnameRules"
              label="Introduce tus apellidos"
              required
              solo
          ></v-text-field>
          <h3 class="font-weight-light">¿Cuál es tu correo electrónico?</h3>
          <v-text-field
              v-model="email"
              :rules="emailRules"
              label="Introduce tu correo electrónico"
              required
              solo
          ></v-text-field>
          <h3 class="font-weight-light">Crea una contraseña</h3>
          <v-text-field
              :append-icon="show2 ? 'mdi-eye' : 'mdi-eye-off'"
              :rules="[rules.required, rules.min]"
              :type="show2 ? 'text' : 'password'"
              name="input-10-2"
              label="Crea una contraseña"
              hint="At least 8 characters"
              value=""
              class="input-group--focused"
              @click:append="show2 = !show2"
              solo
          ></v-text-field>
          <v-card-text class="grey--text">Al registrarse, aceptas los <light class="primary--text text-decoration-underline" >Términos y condiciones</light></v-card-text>
          <v-btn block color="red" class="white--text" height="50" to="/Login">REGÍSTRARTE</v-btn>
        </v-container>
      </v-form>
      <v-divider></v-divider>
      <v-card-actions class="d-flex justify-center mb-2">
        <v-spacer></v-spacer>
        <h4>¿Ya tienes cuenta?</h4>
        <v-spacer></v-spacer>
      </v-card-actions>
      <v-card-actions class="d-flex justify-center mb-2">
            <v-btn
                block
                outlined
            elevation="1"
                height="50"
            class="d-flex justify-center"
                to="Login"
        >INICIA SESIÓN</v-btn>
      </v-card-actions>
    </v-card>
  </app>
</template>

<script>
export default {
  name: "Register",
  data () {
    return {
      show1: false,
      show2: false,
      password: 'Password',
      rules: {
        required: value => !!value || 'Requerido.',
        min: v => v.length >= 8 || 'Mínimo 8 carácteres',
      },
      lastname: '',
      lastnameRules: [
        v => !!v || 'Apellidos son requeridos',
        v => /.+@.+\..+/.test(v) || 'Apellidos deben ser válidos',
      ],
      name: '',
      nameRules: [
        v => !!v || 'Nombre es requerido',
        v => /.+@.+\..+/.test(v) || 'Nombre debe ser válido',
      ],
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