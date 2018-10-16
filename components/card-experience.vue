<template>
  <div>
    <v-toolbar
      color="grey darken-1"
      dark
      class="elevation-10"
    >
      <v-icon dark>card_travel</v-icon>
      <v-toolbar-title>Pengalaman</v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>

    <v-card class="elevation-10">
      <v-container
        fluid
        grid-list-lg
      >
        <div v-for="(item, i) in items" :key="i">
          <v-card-text class="text-xs-justify">
            <span class="headline">{{item.judul}}</span><br>
            <span class="body-2 blue--text">{{item.tahun}}</span><br>
            <span>{{item.deskripsi}}</span>
          </v-card-text>
        </div>
      </v-container>
    </v-card>
  </div>
</template>
<script>
  export default {
    data: () => ({
      items: [
        {judul: 'Kerja Praktek', tahun: '2017', deskripsi: 'Saat kuliah, saya melaksanakan kerja praktek di SMKN 5 Semarang. Saat kerja praktek, ' +
            'saya membuat sistem bimbingan konseling online menggunakan framework laravel untuk membantu mempermudah bimbingan antara ' +
            'murid,orang tua dan guru Bk.'},
      ]
    })
  }
</script>
