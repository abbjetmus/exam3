<template>
  <v-app>
    <v-app-bar
      app
      class="green lighten-1 white--text"
      :elevation="2"
    >
      <v-toolbar-title class="text-h3 font-weight-thin">Exam 3</v-toolbar-title>
      <v-spacer />
      <div>
        <v-btn
          :dark="true"
          depressed
          to="/"
          class="ml-2"
        >
          Home
        </v-btn>

        <v-btn
          depressed
          to="/about"
          class="ml-2"
        >
          About
        </v-btn>

        <v-btn
          depressed
          to="/hello"
          class="ml-2"
        >
          Hello
        </v-btn>
      </div>
    </v-app-bar>
    <v-main>

      <router-view></router-view>

    </v-main>
    <v-footer
      dark
      padless
    >
      <v-card
        flat
        tile
        class="green lighten-1 text-center"
      >
        <v-card-text>
          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4 white--text"
            icon
          >
            <v-icon size="24px">
              {{ icon }}
            </v-icon>
          </v-btn>
        </v-card-text>

        <v-card-text class="white--text pt-0">
          Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
        </v-card-text>

        <v-divider></v-divider>

        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} — <strong>Exam 3</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  data () {
    return {
      drawer: false,
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }
  },
};
</script>
