<template>
<div>
  <v-app>
    <div class="appContainer">
      <Header/>
      <Aboutus/>
      <Services/>
      <Solutions/>
      <Contactus/>
    </div>
  </v-app>
</div>
</template>

<script>
import Header from './components/Header.vue';
import Aboutus from './components/Aboutus.vue';
import Services from './components/Services.vue';
import Solutions from './components/Solutions.vue';
import Contactus from './components/Contactus.vue';

export default {
  name: 'App',

  components: {
    Header,
    Aboutus,
    Services,
    Solutions,
    Contactus
  },

  data: () => ({
    //
  }),
};
</script>
<style scoped>
.appContainer{
  display: flex;
  flex-direction: column;
}
</style>
