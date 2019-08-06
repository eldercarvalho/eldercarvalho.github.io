<template>
  <v-card id="academic" flat class="section mb-5">
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
        <v-list-item>
          <v-list-item-action>
            <img src="@/assets/images/udemy.png" alt="">
          </v-list-item-action>
          <v-list-item-content>
            <p class="title primary--text">JS com TDD na Prática</p>
            <p class="mb-0">Udemy</p>
            <p>Completo em 2019</p>
            <a href="https://www.udemy.com/certificate/UC-BADFA6AU/" target="_blank">Certificado</a>
          </v-list-item-content>
        </v-list-item>
        <v-list-item>
          <v-list-item-action>
            <img src="@/assets/images/udemy.png" alt="">
          </v-list-item-action>
          <v-list-item-content>
            <p class="title primary--text">The Complete JavaScript Course 2019: Build Real Projects!</p>
            <p class="mb-0">Udemy</p>
            <p>Completo em 2018</p>
            <a href="https://www.udemy.com/certificate/UC-0DBWWI77/" target="_blank">Certificado</a>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    
  }),

  methods: {
  
  }
}
</script>

<style lang="scss">

</style>
