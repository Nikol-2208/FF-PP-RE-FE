<template>
  <v-card
      class="mx-auto"
      elevation="0"
  >
    <v-card-actions>
      <v-spacer></v-spacer>
      <v-card-title class="font-weight-bold"><h1>Keiko Sofia Fujimori Higuchi</h1></v-card-title>
      <v-spacer></v-spacer>
    </v-card-actions>
    <v-card max-width="1326" class="mx-auto my-2" elevation="0">
      <v-container  class="d-flex justify-space-around mb-1">
        <v-row no-gutters>
          <v-col cols="3">
            <v-card
                class="mx-auto"
                max-width="248"
                max-height="349"
                elevation="0"
            >
              <v-img
                  src="@/assets/Image (13).png"
                  height="450"
              ><v-icon class="mx-1 my-4" large color="white">mdi-pencil</v-icon></v-img>
            </v-card>
          </v-col>
          <v-col cols="8">
            <v-container  class="d-flex justify-space-around mb-1">
              <v-card

                  max-width="250"
                  max-height="220"
              >
                <v-container>
                  <span><h4>Fecha de nacimiento</h4></span>
                  <span><h5 class="font-weight-light">25 de mayo de 1975</h5></span>
                  <span><h4>Lugar de nacimiento</h4></span>
                  <span><h5 class="font-weight-light">Lima, Perú</h5></span>
                  <span><h4>Profesión</h4></span>
                  <span><h5 class="font-weight-light">Política y administradora</h5></span>
                  <span><h4>Partido político</h4></span>
                  <span><h5 class="font-weight-light">Fuerza Popular</h5></span>
                  <v-icon class="mx-16" color="grey">mdi-pencil</v-icon>
                </v-container>
              </v-card>
              <v-card
                  class="mx-auto"
                  max-width="248"
                  max-height="238"
              >
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-icon class="mx-1" color="grey">mdi-pencil</v-icon>
                  <v-card-title>Biografía</v-card-title>
                  <v-spacer></v-spacer>
                </v-card-actions>
                <v-card-text>Eventos principales acerca de la vida de el/la candidadato/a de interés publico.</v-card-text>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn text color="red">VER</v-btn>
                  <v-spacer></v-spacer>
                </v-card-actions>
              </v-card>
              <v-card
                  class="mx-auto"
                  max-width="248"
                  max-height="238"
              >
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-icon class="mx-1" color="grey">mdi-pencil</v-icon>
                  <v-card-title >Información Legal</v-card-title>
                  <v-spacer></v-spacer>
                </v-card-actions>
                <v-card-text>Casos de investigación y sucesos relacionados a aspectos legales de interés nacional.</v-card-text>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn text color="red">VER</v-btn>
                  <v-spacer></v-spacer>
                </v-card-actions>
              </v-card>
            </v-container>
            <v-col cols="4">
              <v-card></v-card>
            </v-col>
            <v-col  md="10"
                    offset-md="4" >
              <v-card
                  max-height="122"
                  max-width="512">
                <v-container>
                  <span><h4>Aceptación Ciudadana</h4></span>
                  <span><h1>13.41%</h1></span>
                  <span class="font-weight-light"><h4>Elecciones Generales y Parlamento Andino 2021 | Primera vuelta</h4></span>

                </v-container>
              </v-card>
            </v-col>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
    <v-card-title class="font-weight-bold">Últimas publicaciones sobre Keiko Fujimori</v-card-title>
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
  name: "AInformationCandidate"
}
</script>

<style scoped>

</style>