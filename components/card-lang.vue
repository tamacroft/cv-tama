<template>
  <div>
    <v-toolbar
      color="grey darken-1"
      dark
      class="elevation-10"
    >
      <v-icon dark>record_voice_over</v-icon>
      <v-toolbar-title>Bahasa</v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>

    <v-card class="elevation-10">
      <v-container
        fluid
        grid-list-lg
      >
          <v-card-text class="text-xs-justify">
            <div v-for="(item, i) in items" class="pb-2" :key="i">
              <v-checkbox
                v-model="item.bahasa"
                :label="item.bahasa"
                color="green"
                readonly
                checked
              ></v-checkbox>
            </div>
          </v-card-text>
      </v-container>
    </v-card>
  </div>
</template>
<script>
  export default {
    data: () => ({
      items: [
        {bahasa: 'Bahasa Inggris', divider: true},
        {bahasa: 'Bahasa Indonesia', divider: true},
        {bahasa: 'Bahasa Jawa', divider: false},
      ]
    })
  }
</script>
