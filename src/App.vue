<template>
  <v-app>
    <v-app-bar prominent>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-app-bar-title>Logo</v-app-bar-title>
      <v-btn icon>
      <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <v-btn variant="text" icon="mdi-filter"></v-btn>
      <v-btn icon="mdi-dots-vertical"></v-btn>
  </v-app-bar>

<v-navigation-drawer v-model="drawer" permanent color="indigo-darken-4">

</v-navigation-drawer>

  

  
    <v-main>
      <v-card height="300px" class="d-flex align-center justify-space-around">
        <div >
          <v-card height="200px" width="25vw"  class="bg-grey-darken-4 text-white d-flex align-center justify-center">
            <!-- <p class="text-center text-medium-emphasis">
                      Lorem ipsum dolor sit modi commodi nisi. Quaerat veniam expedita sint maxime dolore doloremque quidem aliquam cupiditate atque! Distinctio, cumque!
            </p> -->
          </v-card>
        </div>
        <div>
          <v-card height="200px"  width="25vw"  class="bg-grey-darken-4 text-white d-flex align-center justify-center ">
            <!-- <p class="text-center text-medium-emphasis">
                      Lorem ipsum dolor sit modi commodi nisi. Quaerat veniam expedita sint maxime dolore doloremque quidem aliquam cupiditate atque! Distinctio, cumque!
            </p> -->
          </v-card>
        </div>
        <div>
          <v-card height="200px"  width="25vw" class="bg-grey-darken-4 text-white d-flex align-center justify-center">
            <!-- <p class="text-center text-medium-emphasis">
                      Lorem ipsum dolor sit modi commodi nisi. Quaerat veniam expedita sint maxime dolore doloremque quidem aliquam cupiditate atque! Distinctio, cumque!
            </p> -->
          </v-card>
        </div>
        
      </v-card>

          <v-divider></v-divider>

      <v-card height="300px" class="d-flex align-center justify-space-around">
        <div>
          <v-card height="250px" width="79vw" class="bg-grey-darken-4">

          </v-card>
        </div>
      </v-card>

    <!-- <LoginVue/> -->
    </v-main>

  </v-app>
</template>

<script>
// import LoginVue from './components/LoginVue.vue'
// import NavigationVue from './components/NavigationVue.vue'


export default {
  name: 'App',
  components: {
    // LoginVue,
    // NavigationVue,
  },

  data: () => ({
    //
     drawer: true,
  }),
}
</script>
<style>
  .edit {
    background-color: aqua;
  }
</style>