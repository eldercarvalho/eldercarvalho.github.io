<template>
  <v-card id="experience" flat class="section mb-5">
    <v-card-title class="mb-2" >
      Onde estive
    </v-card-title>
    <v-card-text>
      <v-timeline>
        <v-timeline-item v-for="x in experiences"  :key="x.company">
          <template v-slot:opposite>
            <span class="subtitle-1">{{ x.period }}</span>
          </template>
          <v-card class="elevation-2">
            <v-card-title class="title">{{ x.company }}</v-card-title>
            <v-card-text class="white text--primary">
              <h3 class="mb-1">{{ x.role }}</h3>
              {{ x.activities }}
            </v-card-text>
          </v-card>
        </v-timeline-item>
      </v-timeline>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    experiences: [
      {
        company: 'nuCash',
        role: 'Desenvolvedor JR',
        period: '08/2017 - 07/2019',
        activities: 'Desenvolvimento e manutenção de sistemas front-end, nuCash Dashboard Corporante, aplicativo nuCash IOS, nuCash PDV desktop, elabaração de design system',
        color: 'red lighten-2'
      },
      {
        company: 'Soma Virtual',
        role: 'Desenvolvedor Front-end',
        period: '07/2015 - 08/2017',
        activities: 'Desenvolvimento e manutenção de sistemas front-end, websites, temas para wordpress, aplicativos híbrios.',
        color: 'green lighten-1'
      },
      {
        company: 'TRE-AM',
        role: 'Estagiário em Desenvolvimento Web',
        period: '07/2014 - 07/2015',
        activities: 'Desenvolvimento e manutenção de sistemas web.',
        color: 'purple darken-1'
      },

    ]
  })
}
</script>

<style lang="scss">
.v-timeline {
  max-width: 800px;
  margin: 0 auto;
}
</style>
