<template>
  <v-layout>
    <v-container>
      <v-breadcrumbs class="px-0" :items="navigations"></v-breadcrumbs>
      <v-layout align-center>
        <h1 class="text-h2">Mes cours</h1>
        <v-spacer></v-spacer>
        <v-btn small fab color="success">
          <v-icon>mdi-plus</v-icon>
        </v-btn>
      </v-layout>

      <v-layout class="mt-5">
        <v-row>
          <v-col cols="3" style="position: relative;" v-for="i in 7" :key="i">
            <v-btn style="position: absolute; top: 16px; right: 16px; z-index: 1;" x-small fab @click.stop="test('b')">
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
            <v-card outlined @click.stop="test('a')">
              <v-img
                class="white--text align-end"
                src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
              >
                <v-card-title>Javascript</v-card-title>
              </v-img>

              <v-card-subtitle>14 chapitres</v-card-subtitle>

              <v-card-text class="text--primary">
                <div>JavaScript (qui est souvent abrégé en « JS ») est un langage de script léger, orienté objet, principalement...</div>
              </v-card-text>

            </v-card>
          </v-col>
        </v-row>
      </v-layout>
    </v-container>
  </v-layout>
</template>

<script>
export default {
  data: () => ({
    navigations: [
      {
        text: 'Cours',
        disabled: false,
        href: 'cursus'
      }
    ]
  }),
  methods: {
    test (e = '') {
      alert('Something ' + e)
    }
  }
}
</script>