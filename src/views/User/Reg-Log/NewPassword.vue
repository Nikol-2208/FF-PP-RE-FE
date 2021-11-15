<template>
  <app>
    <v-card
        class="mx-auto my-2"
        max-width="400"
        elevation="0"
    >
      <v-card-title></v-card-title>
      <v-card-title class="text-h4 mb-2">
        Cambiar contraseña
      </v-card-title>
      <v-form class="action">
        <v-container fluid>
          <h3 class="font-weight-light">¿Cuál es tu contraseña actual?</h3>
          <v-text-field
              :append-icon="show2 ? 'mdi-eye' : 'mdi-eye-off'"
              :rules="[rules.required, rules.min]"
              :type="show2 ? 'text' : 'password'"
              name="input-10-2"
              label="Introduce tu contraseña actual"
              hint="At least 8 characters"
              value=""
              class="input-group--focused"
              @click:append="show2 = !show2"
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
          <v-btn block color="red" class="white--text" height="50" to="/password">GUARDAR</v-btn>
        </v-container>
      </v-form>
    </v-card>
  </app>
</template>

<script>
export default {
  name: "NewPassword",
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