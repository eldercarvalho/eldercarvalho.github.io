<template>
  <v-card id="about" flat class="section mb-5">
    <v-card-title class="mb-2">
      Sobre mim
    </v-card-title>
    <v-card-text>
      <div class="chips mb-3">
        <v-chip class="mr-1" outlined color="primary">Brasileiro</v-chip>
        <v-chip class="mr-1" outlined color="primary">Solteiro</v-chip>
        <v-chip class="mr-1" outlined color="primary">26 anos</v-chip>
      </div>
      <v-container fluid>
        <v-layout row wrap>
          <v-flex xs12 md6>
            <p class="body-1">
              Olá! Muito prazer, me chamo Elder, sou desenvolvedor front-end há pouco mais de 3 anos.
              Tenho experiencia com desenvolvimento de websites, sistemas front-end, aplicativos híbridos e nativos para IOS e desktop.
            </p>
            <p class="body-1">Estou sempre em busca de novos desafios.</p>
          </v-flex>
          <!-- <v-flex xs12 md6>
            <img src="@/assets/images/front-end.jpg" alt="">
          </v-flex> -->
        </v-layout>
      </v-container>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data: () => ({
  })
}
</script>

<style>
#about {
  
}
</style>


