<template>
  <v-card
      class="mx-auto"
      elevation="0"
  >
    <v-img
        class="white--text justify-center"
        height="600"
        src="@/assets/palacio.jpg"
        gradient="to top right, rgba(43, 49, 65, 0.9), rgba(96, 125, 139, 0.9)"
    >
      <v-container>
      </v-container>
      <v-container>
      </v-container>
      <v-container>
      </v-container>
      <v-container class="d-flex justify-center mb-14">
        <v-row
            align="center"
            justify="center"
        >
          <v-col class="text-center"  cols="8">
            <h1 class="text-h3 font-weight-bold mb-10">
              Encuentra la información que tanto buscabas
              <v-icon color="white">mdi-pencil</v-icon>
            </h1>
          </v-col>
          <v-col
              class="text-center"
              cols="8"
          >
            <h2 class="text-h4 font-weight-thin mb-6">
              Accede a la informacion de presidentes, partidos políticos y candidatos todo en un solo lugar
              <v-icon color="white">mdi-pencil</v-icon>
            </h2>
          </v-col>
        </v-row>
      </v-container>
      <v-container  class="d-flex justify-space-around mb-10">
        <v-btn width="350" height="50">LÍNEA DEL TIEMPO PRESIDENCIAL <v-icon color="grey">mdi-pencil</v-icon></v-btn>
        <v-btn width="350" height="50">PARTIDOS POLÍTICOS VIGENTES <v-icon color="grey">mdi-pencil</v-icon></v-btn>
        <v-btn width="350" height="50">ELECCIONES GENERALES 2021 <v-icon color="grey">mdi-pencil</v-icon></v-btn>
      </v-container>
      <v-spacer></v-spacer>
    </v-img>
    <v-card-title class="font-weight-bold">Últimas publicaciones</v-card-title>
    <v-container  class="d-flex justify-space-around mb-10">
      <v-card
          class="mx-auto"
          max-width="350"
      >
        <v-img
            src="@/assets/Image (16).png"
            height="200px"
        ></v-img>
        <v-card-title>
          Último debate electoral 2021
        </v-card-title>
        <v-card-subtitle>
          Escrito por Charlie Franci
        </v-card-subtitle>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-icon color="grey">mdi-pencil</v-icon>
        </v-card-actions>
      </v-card>
      <v-card
          class="mx-auto"
          max-width="350"
      >
        <v-img
            src="@/assets/Image (1).png"
            height="200px"
        ></v-img>
        <v-card-title>
          Crisis política en el Perú
        </v-card-title>
        <v-card-subtitle>
          Escrito por Charlie Franci
        </v-card-subtitle>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-icon color="grey">mdi-pencil</v-icon>
        </v-card-actions>
      </v-card>
      <v-card
          class="mx-auto"
          max-width="350"
      >
        <v-img
            src="@/assets/Image (2).png"
            height="200px"
        ></v-img>
        <v-card-title>
          La indecisión ciudadana
        </v-card-title>
        <v-card-subtitle>
          Escrito por Charlie Franci
        </v-card-subtitle>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-icon color="grey">mdi-pencil</v-icon>
        </v-card-actions>
      </v-card>
      <v-card
          class="mx-auto"
          max-width="350"
      >
        <v-img
            src="@/assets/Image (3).png"
            height="200px"
        ></v-img>
        <v-card-title>
          Fin del gobierno de Merino
        </v-card-title>
        <v-card-subtitle>
          Escrito por Charlie Franci
        </v-card-subtitle>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-icon color="grey">mdi-pencil</v-icon>
        </v-card-actions>
      </v-card>
    </v-container>
  </v-card>
</template>

<script>
export default {
  name: "AHome",
  components:{
  }
}
</script>

<style scoped>

</style>