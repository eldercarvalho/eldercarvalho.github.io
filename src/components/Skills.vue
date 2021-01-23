<template>
  <v-card id="skills" class="section mb-5">
    <v-card-title class="mb-2" >
      Habilidades
    </v-card-title>
    <v-card-text>
      <v-container fluid>
        <v-layout row wrap>
          <v-flex xs4 md2 v-for="skill in skills" :key="skill" class="text-center">
            <v-avatar tile class="mr-5 mb-5">
              <img :src="getSkillImage(skill)" :alt="skill" :title="skill">
            </v-avatar>
          </v-flex>
        </v-layout>
      </v-container>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    skills: [
      'Javascript', 
      'Typescript',
      'Vue',
      'Vuex',
      'Vuetify',
      'Angular',
      'jQuery',
      'D3',
      'HTML5',
      'CSS3',
      'Sass',
      'webpack',
      'Gulp',
      'Nodejs',
      'WordPress',
      'Electronjs'
    ]
  }),

  methods: {
    getSkillImage(skill) {
      var images = require.context('../assets/images/skills', false, /\.png$/)
      return images('./' + skill + ".png")
    }
  }
}
</script>

