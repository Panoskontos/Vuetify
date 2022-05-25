<template>
  <v-app>
    <v-app-bar prominent class="bg-grey-darken-4">
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-app-bar-title></v-app-bar-title>
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
        <v-list-item prepend-icon="mdi-account-supervisor-circle" title="Keys" value="supervisors"></v-list-item>
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

<!-- <AlcaliDesignVue/> -->
<v-main class="body ">
    <div height="225px" class="row bg-transparent mt-5 mx-10 d-flex justify-center" >

     <v-hover v-slot="{ isHovering, props }">
      <v-card 
       v-bind="props"
        :class="`elevation-${isHovering ? 24 : 6}`"
      height="225px" width="60%" class="row-card bg-blue-grey-darken-3 mr-10">

      <ConformityComponent/>

      </v-card>      
     </v-hover>
      
      <v-hover v-slot="{ isHovering, props }">
      <v-card 
       v-bind="props"
        :class="`elevation-${isHovering ? 24 : 6}`"
      height="225px" width="20%" class="row-card row-card-keys bg-blue-grey-darken-3 ">

      <KeysComponent/>

</v-card>
      </v-hover>
      
      
      <v-hover v-slot="{ isHovering, props }">
      <v-card 
       v-bind="props"
        :class="`elevation-${isHovering ? 24 : 6}`"
      height="225px" width="28%" class="row-card row-card-status bg-blue-grey-darken-3 ml-10">

  <StatusComponent/>

</v-card>
      </v-hover>      

    </div>
    
    <div  height="200px" class="bg-transparent mx-10 mt-10 d-flex justify-center" > 
        
        <v-hover v-slot="{ isHovering, props }">
      <v-card 
       v-bind="props"
        :class="`elevation-${isHovering ? 24 : 6}`"
        
        height="200px" width="50%" class="bg-blue-grey-darken-3 mr-10">
        </v-card>      
        </v-hover>

    <v-hover v-slot="{ isHovering, props }">
      <v-card 
       v-bind="props"
        :class="`elevation-${isHovering ? 24 : 6}`"
         height="200px" width="50%" class="bg-blue-grey-darken-3 ">
        </v-card>
    </v-hover>     
    
    </div>
    
     <v-hover v-slot="{ isHovering, props }">
    <v-card 
    v-bind="props"
        :class="`elevation-${isHovering ? 24 : 6}`"
    height="320px" class="bg-blue-grey-darken-3 mx-10 mt-10" 
     :style="{ 'background-color': hover ? 'red' : '#BB86FC' }"
    >      
    </v-card>
    </v-hover>
</v-main>
    
  </v-app>
</template>

<script>
// import LoginVue from './components/LoginVue.vue'
// import NavigationVue from './components/NavigationVue.vue'
// import AlcaliDesignVue from './components/AlcaliDesignVue.vue'
import KeysComponent from './components/KeysComponent.vue'
import StatusComponent from './components/StatusComponent.vue'
import ConformityComponent from './components/ConformityComponent.vue'

export default {
  name: 'App',
  components: {
    // LoginVue,
    // NavigationVue,
    // AlcaliDesignVue
    KeysComponent,
    StatusComponent,
    ConformityComponent
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

@media only screen and (max-width: 1000px) {
  .row {
    background-color: rgb(255, 255, 255);
    width: 80%;
    height: 700px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .row-card {
    width: 100% !important;
    margin-bottom: 20px;
    height: 205px !important;
    margin: auto !important;
  }

  .row-card-keys {
    height: 225px !important;
  }

  .row-card-status {
    height: 225px !important;
  }
}

</style>