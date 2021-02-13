<template>
<div>
  <v-app>
    <v-app-bar color="white lighten-3" app clipped-right>
        <v-img
            class="mx-2"
            src="./assets/logo.png"
            height="10vw"
            max-height="50"
            max-width="50"
            contain
        ></v-img>
        <v-spacer></v-spacer>
        <v-app-bar-nav-icon default class="d-sm-none" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        <a class="mx-2 d-none d-sm-block" @click="$vuetify.goTo('#about')">About us</a>
        <a class="mx-2 d-none d-sm-block" @click="$vuetify.goTo('#service')">Services </a>
        <a class="mx-2 d-none d-sm-block" @click="$vuetify.goTo('#solution')">Solutions</a>
        <a class="ml-2 mr-8 d-none d-sm-block" @click="$vuetify.goTo('#contact')">Contact us</a>
        <!-- <span class="mx-1 body-2 d-none d-sm-block">EN</span>
        <span class="mx-1 body-2 d-none d-sm-block">DE</span> -->
        <v-navigation-drawer
        clipped
        mobile-breakpoint
        temporary
        absolute
        disable-resize-watcher
        class="d-sm-none header"
        v-model="drawer"
        right
        height="auto"
        >
            <v-list
                nav
                dense
            >
                <v-list-item-group
                active-class=" text--accent-4"
                >
                <v-list-item>
                    <v-list-item-title @click="$vuetify.goTo('#about')">About us</v-list-item-title>
                </v-list-item>
                <v-list-item>
                    <v-list-item-title @click="$vuetify.goTo('#service')">Services</v-list-item-title>
                </v-list-item>
                <v-list-item>
                    <v-list-item-title @click="$vuetify.goTo('#solution')">Solutions</v-list-item-title>
                </v-list-item>
                <v-list-item>
                    <v-list-item-title @click="$vuetify.goTo('#contact')">Contact us</v-list-item-title>
                </v-list-item>
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>
    </v-app-bar>
    <v-content>    
    <div class="appContainer">
      <Aboutus class="top" id="about"/>
      <Services id="service"/>
      <Solutions id="solution"/>
      <Contactus id="contact"/>
    </div>
    </v-content>
  </v-app>
</div>
</template>

<script>
import Aboutus from './components/Aboutus.vue';
import Services from './components/Services.vue';
import Solutions from './components/Solutions.vue';
import Contactus from './components/Contactus.vue';

export default {
  name: 'App',

  components: {
    Aboutus,
    Services,
    Solutions,
    Contactus
  },

  data: () => ({
    drawer: false,
  }),
};
</script>
<style scoped>
*{
  font-family: SpaceGrotesk !important;
  src: local("SpaceGrotesk"),
   url(./fonts/SpaceGrotesk[wght].ttf) format("truetype");
  font-size: 1.2rem;
  text-align: center;
  color: black !important;
}
.appContainer{
  display: flex;
  flex-direction: column;
}
</style>
