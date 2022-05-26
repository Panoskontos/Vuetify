<template>
  <v-app>
    <v-app-bar prominent class="bg-grey-darken-4">
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-app-bar-title></v-app-bar-title>
      <v-btn icon>
      <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <v-btn variant="text" icon="mdi-bell"></v-btn>
      <v-btn icon="mdi-dots-vertical"></v-btn>
  </v-app-bar>

<v-navigation-drawer v-model="drawer" permanent dark class="bg-indigo"  expand-on-hover
       nav rail>

      <v-list nav class="bg-indigo">
          <v-list-item
            prepend-avatar="https://www.logolynx.com/images/logolynx/s_90/90cdeb260df361a39d97540d9c75a814.png"
            title="CORE NETWORKS"
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



<!-- Icons from -->
<!-- https://icon-sets.iconify.design/mdi/database/ -->
        <v-list nav class="bg-indigo">
       <v-list-item prepend-icon="mdi-view-dashboard" title="Dashboard" value="inbox">
       </v-list-item>
       <br>
        <v-list-item prepend-icon="mdi-vector-circle" title="Minions" value="Minions"></v-list-item>
        <br>
        <v-list-item prepend-icon="mdi-email" title="Users" value="Users"></v-list-item>
        <br>
        <v-list-item prepend-icon="mdi-calendar" title="Jobs" value="Jobs"></v-list-item>
        <br>
        <v-list-item prepend-icon="mdi-clock-end" title="Minions" value="Minions"></v-list-item>
        <br>
        <v-list-item prepend-icon="mdi-clock-start" title="Clock-in" value="clockin"></v-list-item>
        <br>
        <v-list-item prepend-icon="mdi-database" title="Databse" value="clockin"></v-list-item>
        </v-list>

</v-navigation-drawer>

<v-main class="body">
  <!-- <HomeView/> -->
  <MinionsView/>
</v-main>

    
  </v-app>
</template>

<script>
import MinionsView from "./components/MinionsView.vue";
// import HomeView from './components/HomeView.vue'

export default {
  name: 'App',
  components: {
    MinionsView
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
 .body {
    background-color: #1e1e24;
  }


</style>