<template>
  <div>
    <v-toolbar
      color="grey darken-1"
      dark
      class="elevation-10"
    >
      <v-icon dark>sentiment_very_satisfied</v-icon>
      <v-toolbar-title>Hobi</v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>

    <v-card class="elevation-10">
      <v-container
        fluid
        grid-list-md
      >
          <v-card-text class="text-xs-center">
            <v-tooltip bottom>
              <v-icon x-large class="ma-3" slot="activator">audiotrack</v-icon><span>Mendengarkan musik</span>
            </v-tooltip>

            <v-tooltip bottom>
              <v-icon x-large class="ma-3" slot="activator">video_library</v-icon><span>Menonton video</span>
            </v-tooltip>

            <v-tooltip bottom>
              <v-icon x-large class="ma-3" slot="activator">videogame_asset</v-icon><span>Bermain video game</span>
            </v-tooltip>
          </v-card-text>
      </v-container>
    </v-card>
  </div>
</template>
<script>
  export default {
  }
</script>
