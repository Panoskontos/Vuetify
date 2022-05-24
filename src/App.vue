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

<v-navigation-drawer v-model="drawer" permanent dark class="bg-indigo"  expand-on-hover
        rail>


<v-list nav class="bg-indigo">
       <v-list-item prepend-icon="mdi-view-dashboard" title="Inbox" value="inbox"></v-list-item>
        <v-list-item prepend-icon="mdi-account-supervisor-circle" title="Supervisors" value="supervisors"></v-list-item>
        <v-list-item prepend-icon="mdi-email" title="Users" value="Users"></v-list-item>
        <v-list-item prepend-icon="mdi-calendar" title="Jobs" value="Jobs"></v-list-item>
        <v-list-item prepend-icon="mdi-clock-end" title="Minions" value="Minions"></v-list-item>
        <v-list-item prepend-icon="mdi-clock-start" title="Clock-in" value="clockin"></v-list-item>
  </v-list>

</v-navigation-drawer>

  

  
    <v-main>
      <v-card height="300px" class="d-flex align-center justify-space-around">
        <div >
          <v-card height="200px" width="25vw" :elevation="5" class=" rounded-lg bg-grey-darken-4 text-white d-flex align-center justify-center">
            <!-- <p class="text-center text-medium-emphasis">
                      Lorem ipsum dolor sit modi commodi nisi. Quaerat veniam expedita sint maxime dolore doloremque quidem aliquam cupiditate atque! Distinctio, cumque!
            </p> -->
          </v-card>
        </div>
        <div>
          <v-card height="200px"  width="25vw"  class=" rounded-lg bg-grey-darken-4 text-white d-flex align-center justify-center ">
            <!-- <p class="text-center text-medium-emphasis">
                      Lorem ipsum dolor sit modi commodi nisi. Quaerat veniam expedita sint maxime dolore doloremque quidem aliquam cupiditate atque! Distinctio, cumque!
            </p> -->
          </v-card>
        </div>
        <div>
          <v-card height="200px"  width="25vw" class="bg-grey-darken-4 rounded-lg text-white d-flex align-center justify-center">
            <!-- <p class="text-center text-medium-emphasis">
                      Lorem ipsum dolor sit modi commodi nisi. Quaerat veniam expedita sint maxime dolore doloremque quidem aliquam cupiditate atque! Distinctio, cumque!
            </p> -->
          </v-card>
        </div>
        
      </v-card>


      <v-card height="300px" class="d-flex align-center justify-space-around">
        <div>
          <v-card height="250px" width="85vw" class="bg-grey-darken-4">

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
     items: [
          { title: 'Dashboard', icon: 'mdi-view-dashboard' },
          { title: 'Photos', icon: 'mdi-image' },
          { title: 'About', icon: 'mdi-help-box' },
     ]
  }),
}
</script>
<style>
  .edit {
    background-color: aqua;
  }
</style>