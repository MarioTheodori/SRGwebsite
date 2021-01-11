<template>
  <div class="Header">
        <v-app-bar color="white lighten-3">

            <v-img
                class="mx-2"
                src="../assets/logo-02@2x.png"
                max-height="40"
                max-width="40"
                contain
            ></v-img>

            <v-spacer></v-spacer>

            <v-app-bar-nav-icon class="d-sm-none" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
            <span class="mx-2 body-2 d-none d-sm-block">About us</span>
            <span class="mx-2 body-2 d-none d-sm-block">Service </span>
            <span class="mx-2 body-2 d-none d-sm-block">Solutions</span>
            <span class="ml-2 body-2 d-none d-sm-block">Skills</span>
            <span class="ml-2 mr-8 body-2 d-none d-sm-block">Contact us</span>

            <span class="mx-1 body-2 d-none d-sm-block">EN</span>
            <span class="mx-1 body-2 d-none d-sm-block">DE</span>
            
            <v-navigation-drawer
            class="d-sm-none"
            app
            v-model="drawer"
            disable-resize-watcher
            absolute
            right
            height="auto"
            >
                <v-list
                    nav
                    dense
                >
                    <v-list-item-group
                    active-class="deep-purple--text text--accent-4"
                    >
                    <v-list-item>
                        <v-list-item-title>About us</v-list-item-title>
                    </v-list-item>
                    <v-list-item>
                        <v-list-item-title>Services</v-list-item-title>
                    </v-list-item>
                    <v-list-item>
                        <v-list-item-title>Solutions</v-list-item-title>
                    </v-list-item>
                    <v-list-item>
                        <v-list-item-title>Skills</v-list-item-title>
                    </v-list-item>
                    <v-list-item>
                        <v-list-item-title>Contact us</v-list-item-title>
                    </v-list-item>
                    </v-list-item-group>
                </v-list>
            </v-navigation-drawer>
        </v-app-bar>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data: () => ({
      drawer: false,
  })
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.Header{
    text-align: center;
    color: white;
    margin: 0;
    padding: 0;
}

</style>
