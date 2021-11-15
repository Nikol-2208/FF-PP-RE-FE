<template>
  <v-card
      class="mx-auto"
      elevation="0"
  >
    <v-container>
      <v-card-title><h2>BIENVENIDO</h2></v-card-title>
      <v-card-text>Seleccione alguna opción</v-card-text>
    </v-container>
    <v-card class="mx-auto my-16" elevation="0">
      <v-container>
        <v-row>
          <v-col cols="6">
            <v-card
                class="mx-14"
                width="500"
                height="450"
                elevation="1"
                color=#B0BEC5
            >
              <v-container>
                <v-card-title><H5>Período Electoral</H5><p class="mx-2"></p> <v-btn color="grey" class="white--text">HABILITADO</v-btn></v-card-title>
                <v-img src="@/assets/image 3.png"></v-img>
              </v-container>
              <div align="center" class="font-weight-bold">Candidatos</div>
            </v-card>
          </v-col>
          <v-col cols="6">
            <v-card
                class="mx-10"
                width="500"
                height="450"
                elevation="1"
                color=#B0BEC5
            >
              <v-container>
                <v-img src="@/assets/image 4.png" height="380" width="420"></v-img>
              </v-container>
              <div align="center" class="font-weight-bold">Página Principal Usuario</div>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
  </v-card>
</template>

<script>
export default {
  name: "ADPeriod"
}
</script>

<style scoped>

</style>