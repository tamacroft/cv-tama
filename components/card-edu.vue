<template>
  <div>
    <v-toolbar
      color="grey darken-1"
      dark
      class="elevation-10"
    >
      <v-icon dark>school</v-icon>
      <v-toolbar-title>Pendidikan</v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>

    <v-card class="elevation-10">
      <v-container
        fluid
        grid-list-lg
      >
        <div v-for="(item, i) in items" :key="i">
          <v-card-text class="text-xs-justify">
            <span class="headline">{{item.sekolah}}</span><br>
            <span class="body-2 blue--text">{{item.tahun}}</span><br>
            <span>{{item.deskripsi}}</span>
          </v-card-text>
          <div v-show="item.divider">
            <v-divider></v-divider>
          </div>
        </div>
      </v-container>
    </v-card>
  </div>
</template>
<script>
export default {
  data: () => ({
    items: [
      {sekolah: 'Universitas Semarang', tahun: '2014-2018', deskripsi: 'Saya kuliah mengambil program studi S1-Teknik Informatika. ' +
          'Selama 4 semester terakhir saya fokus kepada pengembangan website. Saya lulus dengan meraih IPK 3.88(Cumlaude).', divider: true},
      {sekolah: 'SMA N 11 Semarang', tahun: '2011-2014', deskripsi: 'Di SMA N 11 Semarang, saya masuk kelas IPA, walaupun di SMA saya ' +
          'di kelas IPA, saya mulai menyukai dengan perkembangan teknologi. Untuk itulah saya memutuskan meneruskan kuliah dengan ' +
          'mengambil jurusan IT.', divider: false},
    ]
  })
}
</script>
