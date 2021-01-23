<template>
  <v-card id="portifolio" class="section mb-5">
    <v-card-title class="mb-2" >
      Portifólio
    </v-card-title>
    <v-card-text>
      <v-container grid-list-xl>
        <v-layout row wrap>
          <v-flex xs6 sm4 md3 v-for="p in projects" :key="p.title">
            <v-hover v-slot:default="{ hover }">
              <v-card class="project" :elevation="hover ? 12 : 2" :href="p.link" target="_blank">
                <v-img class="white--text" :src="getProjectImage(p.image)" :alt="p.image" >
                  <v-card-title class="align-end fill-height">
                    <h1 class="title">{{ p.title }}</h1>
                  </v-card-title>
                </v-img>
              </v-card>
            </v-hover>
          </v-flex>
        </v-layout>
      </v-container>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    projects: [
      {
        title: 'Amazônico',
        link: 'http://www.amazonico.com.br/',
        image: 'amazonico'
      },
      {
        title: 'Soma Virtual',
        link: 'https://somavirtual.com.br/',
        image: 'somavirtual'
      },
      {
        title: 'Grupo Chibatão',
        link: 'http://www.grupochibatao.com.br/',
        image: 'chibatao'      
      },
      {
        title: 'Dra. Tatiana Teles',
        link: 'http://neuropediatrica.com.br/',
        image: 'tatianateles'
      },
      {
        title: 'Kizem Adivocacia',
        link: 'http://kizemadvocacia.com.br/',
        image: 'kizem'
      },
      {
        title: 'Soma Cursos Odonto',
        link: 'http://somacursosodonto.com.br/',
        image: 'somacursos'
      },
      {
        title: 'Dr. Jefferson Medeiros',
        link: 'http://www.jeffersonmedeiros.com.br/',
        image: 'jeffersonmedeiros'
      },
      {
        title: 'Paulo Pedrosa Headhunder & HR Solutions',
        link: 'http://paulapedrosa.com.br/',
        image: 'paulopedrosa'
      },
      {
        title: 'Projett',
        link: 'http://projett.com.br/',
        image: 'projett'
      },
      {
        title: 'Dr. Eugênio Rocha Jr.',
        link: 'http://www.dreugeniorocha.com.br/',
        image: 'eugeniorocha'
      },
      {
        title: 'Instituto Senescer',
        link: 'https://www.institutosenescer.com.br/'
      },
      {
        title: 'Amazongás',
        link: 'https://www.amazongas.com.br/',
        image: 'amazongas'
      },
      {
        title: 'Orthopaedica',
        link: 'https://orthopaedica.com.br/',
        image: 'orthopaedica'
      },
      {
        title: 'Dra. Caroline Frota',
        link: 'http://www.clinicascarolinefrota.com.br/',
        image: 'carolinefrota'
      },
      {
        title: 'Dra. Isy Peixoto',
        link: 'https://www.isypeixoto.com.br/',
        image: 'isypeixoto'
      },
      {
        title: 'HW Hospitalar',
        link: 'http://hwhospitalar.com.br/',
        image: 'hwhospitalar'
      },
      {
        title: 'Dra. Eline Farias',
        link: 'http://www.draelinefarias.com.br/',
        image: 'elinefarias'
      },
      {
        title: 'Shalom Festas',
        link: 'http://www.shalomfestasmanaus.com.br/',
        image: 'shalomfestas'
      },
      {
        title: 'Mulher a Mil',
        link: 'http://www.mulheramil.com/',
        image: 'mulheramil'
      },
      {
        title: 'Derma',
        link: 'http://dermamanaus.com.br/',
        image: 'derma'
      },
      {
        title: 'Angiolaser',
        link: 'http://www.angiolaser.com.br/',
        image: 'angiolaser'
      },
      {
        title: 'Ortofácil',
        link: 'https://www.ortofacil.com.br/',
        image: 'ortofacil'
      },
      {
        title: 'Dermplast',
        link: 'http://www.dermplast.com/',
        image: 'default'
      },
      {
        title: 'Lauschner',
        link: 'http://www.lauschner.net.br/',
        image: 'lauschner'
      },
      {
        title: 'Dra. Adriana Mariano',
        link: 'https://www.adrianamariano.com.br/',
        image: 'adrianamariano'
      },
      {
        title: 'Dr. Cristiano Paiva',
        link: 'http://www.drcristianopaiva.com.br/',
        image: 'cristianopaiva'
      },
      {
        title: 'Endogastromed',
        link: 'http://www.endogastromed.com.br/',
        image: 'endodastromed'
      },
      {
        title: 'Dra. Savana Maia',
        link: 'http://savanamaia.com/',
        image: "savanamaia"
      },
      {
        title: 'Senhor da História',
        link: 'http://www.senhordahistoria.com.br/'
      },
      {
        title: 'RoraimaNET',
        link: 'http://roraimanet.com.br/',
        image: 'roraimanet'
      },
      {
        title: 'One Clinic',
        link: 'http://oneclinic.net.br/',
        image: 'oneclinic'
      }
    ]
  }),

  methods: {
    getProjectImage(p) {
      var images = require.context('../assets/images/portifolio', false, /\.jpg$/)
      return images('./' + (p || 'default' ) + ".jpg")
    }
  }
}
</script>

<style lang="scss">
#portifolio {
  .project {
    .title {
      background: rgba(#000, 0.5);
      line-height: 1.3;
      padding: 8px;
      border-radius: 5px;
    }
  }
}
</style>
