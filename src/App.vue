<template>
  <v-app>
    <v-navigation-drawer dark v-model="drawer" app>
      <v-card flat color="transparent">
        <v-card-text class="text-center">

          <v-avatar size="150" class="mb-3">
            <img src="@/assets/images/elder.jpg" alt="avatar" />
          </v-avatar>
     
          <h1 class="headline">Elder Carvalho</h1>
          <p class="font-weight-light">Desenvolvedor Front-end</p>
        </v-card-text> 
      </v-card>

      <v-list class="menu">
        <v-list-item v-for="item in menu" :key="item.title" @click="$vuetify.goTo(item.section, options)">
          <v-list-item-action>
            <v-icon size="20">{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-card color="transparent" flat> 
        <v-card-text>
          <p class="mb-1">
            <v-icon small class="mr-1">fa-envelope</v-icon> eld.carv@gmail.com
          </p>
          <p>
            <v-icon small class="mr-1">fa-phone</v-icon> (92) 99527-3094
          </p>
        </v-card-text>
      </v-card>
    </v-navigation-drawer>

    <v-app-bar app flat>
      <v-app-bar-nav-icon @click="drawer = !drawer" color="primary"></v-app-bar-nav-icon>
      <v-toolbar-title class="headline" v-if="!drawer">
        <span>Elder Carvalho</span><span class="font-weight-light subtitle-1"> Desenvolvedor Front-end</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon color="primary" href="https://github.com/eldercarvalho" target="_blank">
        <v-icon>fa-github</v-icon>
      </v-btn>
      <v-btn icon color="primary" href="https://www.linkedin.com/in/elder-carvalho-28753492/" target="_blank">
        <v-icon>fa-linkedin</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content dark>
      <v-container class="main-container" fluid>
        
        <About />

        <Skills />

        <Experience />

        <Academic />

        <Portifolio />

      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import About from "./components/About";
import Skills from "./components/Skills";
import Experience from "./components/Experience";
import Academic from "./components/Academic";
import Portifolio from "./components/Portifolio";

export default {
  name: "App",
  components: {
    About,
    Skills,
    Experience,
    Academic,
    Portifolio
  },
  data: () => ({
    drawer: true,
    menu: [
      { icon: 'fa-user', title: 'Sobre mim', section: '#about' },
      { icon: 'fa-cog', title: 'Habilidades', section: '#skills' },
      { icon: 'fa-map-marker', title: 'Onde estive', section: '#experience' },
      { icon: 'fa-graduation-cap', title: 'Formação', section: '#academic' },
      { icon: 'fa-th', title: 'Portifólio', section: '#portifolio' }
    ],
    options: {
      duration: 600
    }
  })
};
</script>

<style lang="scss">
.v-navigation-drawer {
  background: #191923 !important;
}

.menu {
  .v-list-item__title {
    /* font-weight: lighter !important; */
  }
}

.main-container {
  max-width: 1100px;
}

.section {
  border: 1px solid rgba(#000, 0.05) !important;
}

img {
  max-width: 100%;
}
</style>

