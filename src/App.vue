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
       nav rail>

      <v-list nav class="bg-indigo">
          <v-list-item
            prepend-avatar="https://www.logolynx.com/images/logolynx/s_90/90cdeb260df361a39d97540d9c75a814.png"
            title="BALCALI"
          ></v-list-item>
      </v-list>

        <v-divider></v-divider>

<v-list nav class="bg-indigo">
          <v-list-item
            prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg"
            title="Panos Kontos"
            subtitle="panos@gmailcom"
          ></v-list-item>
      </v-list>

        <v-divider></v-divider>

<v-list nav class="bg-indigo">
       <v-list-item prepend-icon="mdi-view-dashboard" title="Inbox" value="inbox">
       </v-list-item>
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
          <v-card height="200px" width="25vw" :elevation="5" class=" rounded-lg bg-grey-darken-4 text-white ">
         
    <div class="text-center">
      Conformity
    </div>     
         
    <div class="mt-4" >
    <v-progress-linear
      v-model="power"
      color="indigo-darken-4"
      height="25"
     >
      <v-progress-linear
        model-value="25"
        color="yellow"
        height="25"
        reverse
        >
        
      </v-progress-linear>
    </v-progress-linear>

    <br>

    <v-progress-linear
      v-model="skill"
      color="blue-grey"
      height="25"
    >
      <v-progress-linear
        model-value="45"
        color="cyan"
        height="25"
        reverse
        >
        
      </v-progress-linear>
    </v-progress-linear>

    <br>

    <v-progress-linear
      v-model="knowledge"
      height="25"
    >
    <v-progress-linear
        model-value="35"
        color="cyan"
        height="25"
        reverse
        >
      </v-progress-linear>
      <v-progress-linear
        model-value="100"
        color="red"
        height="25"
        reverse
        >
        
      </v-progress-linear>
    </v-progress-linear>
  </div>
        </v-card>
        </div>
        <div>
          <v-card height="200px"  width="25vw"  class=" rounded-lg bg-grey-darken-4 ">
  
  <div class="text-center">
    Keys
  </div>
  <v-table class="mt-4" height="130px" theme="dark" density="compact">
    <thead >
      <tr>
      </tr>
    </thead>
    <tbody>
      <tr
        v-for="item in items"
        :key="item.name"
      >
        <td>{{ item.title }}</td>
        <td>{{ item.status }}</td>
      </tr>
    </tbody>
  </v-table>
          </v-card>
        </div>
        <div>
          <v-card height="200px"  width="25vw" class="bg-grey-darken-4 rounded-lg text-white d-flex align-center justify-center flex-column">
          
  <div class="text-center">
    Keys
  </div>
  <v-table class="mt-4" height="130px" theme="dark" density="compact">
    <thead >
      <tr>
      </tr>
    </thead>
    <tbody>
      <tr
        v-for="item in items"
        :key="item.name"
      >
        <td>{{ item.title }}</td>
        <td>{{ item.status }}</td>
      </tr>
    </tbody>
  </v-table>
  
          </v-card>
        </div>
        
      </v-card>


      <v-card height="300px" class="d-flex  align-center justify-space-around">
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
          { title: 'Accepted', status:5 },
          { title: 'Pending', status:0 },
          { title: 'Rejected', status:0 },
          { title: 'Denied', status:0 },
          
     ],
      skill: 76,
      knowledge: 33,
      power: 78,
  }),
}
</script>
<style>
  .edit {
    background-color: aqua;
  }
</style>