<template>
  <v-layout row>
      <v-flex xs12 md4>
        <v-card color="indigo lighten-1" class="white--text elevation-10">
          <v-img
            src="foto2.jpg"
          ></v-img>
          <div class="px-3 pb-3">
            <v-card-title>
              <span class="title">{{nama}}</span>
              <span class="subheading">Web developer</span>
            </v-card-title>
            <v-divider></v-divider>

            <v-card-text class="text-xs-justify">
              <span>{{tentang}}</span>
            </v-card-text>
            <v-divider></v-divider>

            <v-card-title>
              <span class="title">Skills</span>
            </v-card-title>
           <v-card-text>

             <v-checkbox
               v-for="(item,i) in skills"
               :key="i"
               :label="item.skill"
               v-model="item.skill"
               checked
               readonly
               dark
               color="white"
             ></v-checkbox>
             <!--<div v-for="(item, i) in skills" :key="i">-->
               <!--<span>{{item.skill}}</span>-->
               <!--<v-progress-linear-->
                 <!--color="white"-->
                 <!--height="5"-->
                 <!--:value="item.value"-->
               <!--&gt;</v-progress-linear>-->
             <!--</div>-->
           </v-card-text>
            <v-divider></v-divider>

            <v-card-title>
              <span class="title">Kontak</span>
            </v-card-title>
            <v-card-text>
              <div v-for="(item, i) in kontak" :key="i" class="mb-2">
                <v-icon dark class="mr-4">{{item.icon}}</v-icon><span>{{item.text}}</span>
              </div>
            </v-card-text>
          </div>
        </v-card>
      </v-flex>

      <v-flex xs12 md8>
        <card-edu class="pb-3"></card-edu>
        <card-pengalaman class="pb-3"></card-pengalaman>
        <v-layout row>
          <v-flex d-flex>
            <card-interest class="mr-3"></card-interest>
            <card-lang></card-lang>
          </v-flex>
        </v-layout>
      </v-flex>
  </v-layout>
</template>

<script>
  import CardEdu from '@/components/card-edu'
  import CardPengalaman from '@/components/card-experience'
  import CardInterest from '@/components/card-interest'
  import CardLang from '@/components/card-lang'

export default {
    data: () => ({
      nama: 'Wiratama Adi Wibawa',
      tentang: 'Menjadi seorang web developer adalah pekerjaan yang saya suka. ' +
        'Saya mendalami Laravel dan Vue.js dalam kurun waktu 2 tahun yang lalu. ' +
        'Saat kerja praktik pada tahun 2017, saya membuat sistem bimbingan konseling di SMK 5 menggunakan Framework Laravel. ' +
        'Dalam waktu 1 semester, saya mampu menyelesaikan proyek tugas akhir saya yang menggunakan Nuxt.js dan Firebase. ',
      skills: [
        {skill: 'HTML', value: '95'},
        {skill: 'CSS', value: '80'},
        {skill: 'PHP (Laravel)', value: '70'},
        {skill: 'JS (Vue)', value: '75'},
        {skill: 'SQL', value: '60'}
      ],
      kontak: [
        {icon: 'phone', text: '089698977368'},
        {icon: 'home', text: 'Pancursari No. 72 RT06 RW04'},
        {icon: 'email', text: 'tamacroft.dev@gmail.com'},
      ]
    }),
    components: {
      CardEdu, CardPengalaman, CardInterest, CardLang
    }
}
</script>
<style>
  .v-input--selection-controls__ripple{
    cursor: default
  }
  .v-input--selection-controls__input + .v-label{
    cursor: default;
  }
</style>
