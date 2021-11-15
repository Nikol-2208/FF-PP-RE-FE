<template>
  <v-container class="mx-auto my-14">
    <div>
      <v-container>
        <v-card-title><h1>Publicaciones</h1></v-card-title>
      </v-container>
    </div>
    <v-data-table
        :headers="headers"
        :items="publications"
        sort-by="autor"
        class="elevation-1"
    >
      <template v-slot:top>
        <v-toolbar
            flat
        >
          <v-spacer></v-spacer>
          <v-dialog
              v-model="dialog"
              max-width="500px"
          >
            <template v-slot:activator="{ on, attrs }">
              <v-btn class="mb-2 white--text" color=#607D8B>
                VOLVER
              </v-btn>
              <p class="mx-2"></p>
              <v-btn
                  color="red"
                  dark
                  class="mb-2 white--text"
                  v-bind="attrs"
                  v-on="on"
              >
                + Agregar
              </v-btn>
            </template>
            <v-card>
              <v-card-title>
                <span class="text-h5">{{ formTitle }}</span>
              </v-card-title>

              <v-card-text>
                <v-container>
                  <v-row>
                    <v-col
                        cols="12"
                        sm="6"
                        md="4"
                    >
                      <v-text-field
                          v-model="editedItem.name"
                          label="Título"
                      ></v-text-field>
                    </v-col>
                    <v-col
                        cols="12"
                        sm="6"
                        md="4"
                    >
                      <v-text-field
                          v-model="editedItem.autor"
                          label="Autor"
                      ></v-text-field>
                    </v-col>
                    <v-col
                        cols="12"
                        sm="6"
                        md="4"
                    >
                      <v-text-field
                          v-model="editedItem.tags"
                          label="Tags"
                      ></v-text-field>
                    </v-col>
                    <v-col
                        cols="12"
                        sm="6"
                        md="4"
                    >
                      <v-text-field
                          v-model="editedItem.tipo"
                          label="Tipo"
                      ></v-text-field>
                    </v-col>
                    <v-col
                        cols="12"
                        sm="6"
                        md="4"
                    >
                      <v-text-field
                          v-model="editedItem.date"
                          label="Fecha de publicación"
                      ></v-text-field>
                    </v-col>
                    <v-col
                        cols="12"
                        sm="6"
                        md="4"
                    >
                      <v-text-field
                          v-model="editedItem.supervisor"
                          label="Supervisor"
                      ></v-text-field>
                    </v-col>
                  </v-row>
                </v-container>
              </v-card-text>

              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn
                    color="red"
                    text
                    @click="close"
                >
                  Cancel
                </v-btn>
                <v-btn
                    color=#607D8B;
                    text
                    @click="save"
                >
                  Save
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-dialog>
          <v-dialog v-model="dialogDelete" max-width="500px">
            <v-card>
              <v-card-title class="text-h5">¿Está seguro que quiere eliminar esta publicación?</v-card-title>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn color="red" text @click="closeDelete">Cancel</v-btn>
                <v-btn color="red" text @click="deleteItemConfirm">OK</v-btn>
                <v-spacer></v-spacer>
              </v-card-actions>
            </v-card>
          </v-dialog>
        </v-toolbar>
      </template>
      <template v-slot:item.actions="{ item }">
        <v-icon
            large
            class="mr-2"
            @click="editItem(item)"
        >
          mdi-pencil
        </v-icon>
        <v-icon
            large
            @click="deleteItem(item)"
        >
          mdi-delete
        </v-icon>
      </template>
      <template v-slot:no-data>
        <v-btn
            color="primary"
            @click="initialize"
        >
          Reset
        </v-btn>
      </template>
    </v-data-table>
  </v-container>
</template>

<script>
export default {
  name: "Publications",
  data: () => ({
    dialog: false,
    dialogDelete: false,
    headers: [
      {
        text: 'Título',
        align: 'start',
        sortable: false,
        value: 'name',
      },
      { text: 'Autor', value: 'autor' },
      { text: 'Tags', value: 'tags' },
      { text: 'Tipo', value: 'tipo' },
      { text: 'Fecha de publicación', value: 'date' },
      { text: 'Supervisor', value: 'supervisor' },
      { text: 'Actions', value: 'actions', sortable: false },
    ],
    publications: [],
    editedIndex: -1,
    editedItem: {
      name: '',
      autor: '',
      tags: '',
      tipo: '',
      date: '',
      supervisor: '',
    },
    defaultItem: {
      name: '',
      autor: '',
      tags: '',
      tipo: '',
      date: '',
    },
  }),

  computed: {
    formTitle () {
      return this.editedIndex === -1 ? 'New Item' : 'Edit Item'
    },
  },

  watch: {
    dialog (val) {
      val || this.close()
    },
    dialogDelete (val) {
      val || this.closeDelete()
    },
  },

  created () {
    this.initialize()
  },

  methods: {
    initialize () {
      this.publications = [
        {
          name: 'Último debate electoral 2021',
          autor: 'Charlie Franci',
          tags: 'general, pedro_castillo, keiko_fujimori',
          tipo: 'Artículo',
          date: '30-05-2021',
          supervisor: 'Aldo Vera',
        },
        {
          name: 'Crisis política en el Perú',
          autor: 'Charlie Franci',
          tags: 'general',
          tipo: 'Artículo',
          date: '12-04-2020',
          supervisor: 'Aldo Vera',
        },
        {
          name: 'La indecisión ciudadana',
          autor: 'Charlie Franci',
          tags: 'general',
          tipo: 'Artículo',
          date: '26-10-2020',
          supervisor: 'Aldo Vera',
        },
        {
          name: 'Fin de gobierno de Merino',
          autor: 'Charlie Franci',
          tags: 'general',
          tipo: 'Artículo',
          date: '15-11-2020',
          supervisor: 'Aldo Vera',
        },
        {
          name: 'Fujimorismo en el Perú',
          autor: 'Charlie Franci',
          tags: 'keiko, fujimori',
          tipo: 'Artículo',
          date: '05-05-2020',
          supervisor: 'Aldo Vera',
        },
      ]
    },

    editItem (item) {
      this.editedIndex = this.publications.indexOf(item)
      this.editedItem = Object.assign({}, item)
      this.dialog = true
    },

    deleteItem (item) {
      this.editedIndex = this.publications.indexOf(item)
      this.editedItem = Object.assign({}, item)
      this.dialogDelete = true
    },

    deleteItemConfirm () {
      this.publications.splice(this.editedIndex, 1)
      this.closeDelete()
    },

    close () {
      this.dialog = false
      this.$nextTick(() => {
        this.editedItem = Object.assign({}, this.defaultItem)
        this.editedIndex = -1
      })
    },

    closeDelete () {
      this.dialogDelete = false
      this.$nextTick(() => {
        this.editedItem = Object.assign({}, this.defaultItem)
        this.editedIndex = -1
      })
    },

    save () {
      if (this.editedIndex > -1) {
        Object.assign(this.publications[this.editedIndex], this.editedItem)
      } else {
        this.publications.push(this.editedItem)
      }
      this.close()
    },
  },
}
</script>

<style scoped>

</style>