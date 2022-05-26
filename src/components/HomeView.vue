<template>
    <div>
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
        
        height="230px" width="50%" class="bg-blue-grey-darken-3 mr-10">
        </v-card>      
        </v-hover>

    <v-hover v-slot="{ isHovering, props }">
      <v-card 
       v-bind="props"
        :class="`elevation-${isHovering ? 24 : 6}`"
         height="230px" width="50%" class="bg-blue-grey-darken-3 ">
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

    </div>
</template>

<script>
    import KeysComponent from './KeysComponent.vue'
    import StatusComponent from './StatusComponent.vue'
    import ConformityComponent from './ConformityComponent.vue'

export default {
  name: 'HomeView',
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
 
@media only screen and (max-width: 1000px) {
  .row {
    background-color: rgb(255, 255, 255);
    width: 80%;
    height: 750px;
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