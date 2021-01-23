<template>
  <v-card id="about" class="section mb-5">
    <v-card-title class="mb-2">
      Sobre mim
    </v-card-title>
    <v-card-text>
      <v-container fluid>
        <v-layout row wrap>
          <v-flex xs12 md6>
            <div class="chips mb-3">
              <v-chip class="mr-1" outlined color="primary">Brasileiro</v-chip>
              <v-chip class="mr-1" outlined color="primary">Solteiro</v-chip>
              <v-chip class="mr-1" outlined color="primary">28 anos</v-chip>
            </div>

            <p class="body-1">
              Sou dev front-end há 6 anos, tenho experiência com desenvolvimento de sistemas front-end web,
              mobile e desktop. No momento domino as stacks de Vue.js e React (já trabalhei com Angular
              também mas to um pouco desatualizado hehe). Tento aprender um pouco de outras áreas, gosto de
              desenvolver aplicações back-end como API's Restful (GraphQL em breve) com Node.js e Express
              e to tentando aprender um pouco de devops. Sou um dev detalhista, proativo e autodidata que gosta de desafios. 
            </p>
          </v-flex>

          <v-flex class="d-flex justify-center" xs12 md6>
            <img src="@/assets/images/elder-about.jpg" alt="">
          </v-flex>
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

<style lang="scss">
#about {
  img {
    width: 250px;
    border-radius: 50%;
    /* margin-left: auto; */
  }
}
</style>


