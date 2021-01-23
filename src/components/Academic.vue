<template>
  <v-card id="academic" class="section mb-5">
    <v-card-title class="mb-2" >
      Formação
    </v-card-title>
    <v-card-text>
      <v-list>
        <v-subheader>Graduação</v-subheader>

        <v-list-item>
          <v-list-item-action>
            <img src="@/assets/images/unip.png" alt="">
          </v-list-item-action>

          <v-list-item-content>
            <p class="title primary--text">Ciência da Computação</p>
            <p class="mb-0">Univerdidade Paulista - UNIP</p>
            <p>Completo em 2016</p>
          </v-list-item-content>
        </v-list-item>
        
        <v-divider></v-divider>
        
        <v-subheader>Cursos</v-subheader>

        <v-list-item v-for="course in courses" :key="course.id">
          <v-list-item-action>
            <img :src="`/img/${course.image}.png`" :alt="course.institution">
          </v-list-item-action>
          
          <v-list-item-content>
            <p class="title primary--text">{{ course.title }}</p>
            <p class="mb-0">{{ course.institution }}</p>
            <p>Completo em {{course.year}}</p>
            <a :href="course.link" target="_blank">Certificado</a>
          </v-list-item-content>
        </v-list-item>

      </v-list>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    courses: [
      {
        id: 1,
        title: 'Modern React with Redux',
        institution: 'Udemy',
        year: 2019,
        image: 'udemy',
        link: 'https://www.udemy.com/certificate/UC-5DZ7S8AD/'
      },
      {
        id: 2,
        title: 'JS com TDD na Prática',
        institution: 'Udemy',
        year: 2019,
        image: 'udemy',
        link: 'https://www.udemy.com/certificate/UC-BADFA6AU/'
      },
      {
        id: 3,
        title: 'The Complete JavaScript Course 2019: Build Real Projects!',
        institution: 'Udemy',
        year: 2018,
        image: 'udemy',
        link: 'https://www.udemy.com/certificate/UC-0DBWWI77/'
      }
    ]
  }),

  methods: {
  
  }
}
</script>

<style lang="scss">

</style>
