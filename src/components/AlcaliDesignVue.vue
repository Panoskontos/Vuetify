<template>
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
    Status
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
        <td>Jobs</td>
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

</template>