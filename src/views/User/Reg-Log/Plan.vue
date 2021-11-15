<template>
  <v-app>
    <v-card
        class="mx-auto my-2"
        max-width="400"
        elevation="0"
    >
      <v-card-title></v-card-title>
      <v-card-title></v-card-title>
      <v-card-title class="text-h4 mb-2">
        Cambiar plan
      </v-card-title>
      <v-card
          color="rgba(96, 125, 139, 1), rgba(43, 49, 65, 1)"
          gradient="to top right, rgba(43, 49, 65, 0.9), rgba(96, 125, 139, 0.9)">
        <v-card-text class="white--text">Plan: Premium</v-card-text>
        <v-card-title class="white--text">$19.99 / mensual</v-card-title>
        <v-card-text class="white--text">Accede a la información sobre presidentes, partidos políticos y candidatos.
          Accede sin límites a información exclusiva: Análisis e informes exclusivamente desarrollados para Piensa Perú.</v-card-text>
      </v-card>
      <v-card-actions class="d-flex justify-center mb-2">
        <v-dialog v-model="dialog"
                  width="500">
          <template v-slot:activator="{ on, attrs }">
              <v-btn block color="red" class="white--text" height="50" v-bind="attrs"
                     v-on="on">CONTINUAR LA COMPRA</v-btn>
          </template>
          <v-card>
            <v-img  src="@/assets/money.gif" height="200">
              <div align="center">
                <h1 class="white--text my-6" >¡GRACIAS POR SU SUBSCRIPCRIÓN!</h1>
                <v-btn text color="red" class="text-h6 font-weight-bold" to="/">CERRAR</v-btn>
              </div>
            </v-img>
          </v-card>
        </v-dialog>
      </v-card-actions>
    </v-card>
  </v-app>
</template>

<script>
export default {
  name: "Plan"
}
</script>

<style scoped>

</style>