<template>
<div>
  <v-app>
    <div class="appContainer">
      <Aboutus/>
      <Services/>
      <Solutions/>
      <Contactus/>
    </div>
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
