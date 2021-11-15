<template>
  <v-card
      class="mx-auto"
      elevation="0"
      width="1400"
  >
    <v-card class="mx-auto my-16" elevation="0">
      <v-container>
        <v-row>
          <v-col cols="5">
            <v-card
                class="mx-10"
                width="500"
                height="545"
                elevation="0"
            >
              <v-card-title><H1>PERFIL</H1></v-card-title>
              <v-container>
                <p> <v-icon large color=#6200EE>mdi-alpha-c-circle</v-icon>Nombre</p>
                <v-text-field
                    value="John"
                    label="Solo"
                    solo
                    readonly
                ></v-text-field>
                <p>Apellido</p>
                <v-text-field
                    value="Doe"
                    label="Solo"
                    solo
                    readonly
                ></v-text-field>
                <p>Correo</p>
                <v-text-field
                    value="chrl_fr@gmail.com"
                    label="Solo"
                    solo
                    readonly
                ></v-text-field>
                <p>Contraseña</p>
                <v-text-field
                    value="**********"
                    label="Solo"
                    solo
                    readonly
                ></v-text-field>
              </v-container>
            </v-card>
          </v-col>
          <v-col cols="1">
            <div>
              <v-divider vertical class="mx-auto"></v-divider>
            </div>
            <v-divider vertical class="mx-14 my-auto" color="black" ></v-divider>
          </v-col>
          <v-col cols="5">
            <v-card
                width="550"
                height="530"
                class="mx-11"
                elevation="0"
            >
              <v-card-title><H1>HISTORIAL DE CAMBIOS</H1></v-card-title>
              <v-row>
                <v-col
                    cols="12"
                >
                  <v-card elevation="0">
                    <v-list three-line>
                      <template v-for="(item, index) in items.slice(0, 12)">
                        <v-subheader
                            v-if="item.header"
                            :key="item.header"
                        >
                        </v-subheader>
                        <v-divider
                            v-else-if="item.divider"
                            :key="index"
                            :inset="item.inset"
                        ></v-divider>
                        <v-list-item
                            v-else
                            :key="item.title"
                        >
                          <v-list-item-content>
                            <v-list-item-title v-html="item.title"></v-list-item-title>
                            <v-list-item-subtitle v-html="item.subtitle"></v-list-item-subtitle>
                          </v-list-item-content>
                          <v-list-item-avatar>
                            <v-list-item-title v-html="item.date"></v-list-item-title>
                          </v-list-item-avatar>
                        </v-list-item>
                      </template>
                    </v-list>
                  </v-card>
                </v-col>
              </v-row>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-card>
    <v-btn color=#607D8B class="white--text">VOLVER</v-btn>
  </v-card>
</template>

<script>
export default {
  name: "Profile",
  data: () => ({
    items: [
      { date: '30-05-2021', title: 'Actualización de contenido', subtitle: `Publicación: Último debate electoral 2021` },
      { divider: true, inset: true },
      { date: '12-04-2020', title: 'Actualización de contenido', subtitle: `Publicación: Último debate electoral 2021` },
      { divider: true, inset: true },
      { date: '26-10-2020', title: 'Actualización de contenido', subtitle: `Publicación: Último debate electoral 2021` },
      { divider: true, inset: true },
      { date: '15-11-2020', title: 'Actualización de contenido', subtitle: `Publicación: Último debate electoral 2021` },
      { divider: true, inset: true },
      { date: '05-05-2020', title: 'Actualización de contenido', subtitle: `Publicación: Último debate electoral 2021` },
    ],
  }),
}
</script>

<style scoped>

</style>