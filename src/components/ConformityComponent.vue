<template>
<div>
    <div class="px-10 pt-3 d-flex text-grey-lighten-1 justify-start">
        <h3>Conformity</h3>
    </div>
    <!-- row -->
    <div class=" px-10 mt-5 d-flex justify-space-between align-center">
        <div class="text-grey">
            HIGHSTATE
        </div>
        <v-card width="80%" height="18px" class="rounded-0 bg-transparent ">
            <LinearChart/>
        </v-card>
    </div>
    <!-- row -->
    <div class="px-10 mt-5 d-flex justify-space-between align-center">
        <div class="text-grey">
            PYVERSION
        </div>
        <v-card width="80%" height="18px" class="rounded-0 bg-transparent ">
            <div >
    <v-progress-linear
      model-value="75"
      background-color="green lighten-1"
      color="green-lighten-2"
      height="18"
    >
    
    <v-progress-linear
      model-value="35"
      color="green"
      height="18"
    >
    
    
    </v-progress-linear>
    </v-progress-linear>
    </div>
        </v-card>
    </div>
    <!-- row -->
    <div class="px-10 mt-5 d-flex justify-space-between align-center">
        <div class="text-grey" style="width:97px">
        FOO
        </div>
        <v-card width="80%" height="18px" class="rounded-0 bg-transparent ">
        
            <div >
    <v-progress-linear
      model-value="45"
      background-color="blue lighten-1"
      color="blue-lighten-2"
      buffer-value="65"
      height="18"
    >
    
    <v-progress-linear
      model-value="15"
      color="blue"
      buffer-value="65"
      height="18"
    >
    
    
    </v-progress-linear>
    </v-progress-linear>
    </div>
        </v-card>
    </div>

</div>
</template>


<script>
import LinearChart from './LinearChart.vue'

export default {
    components:{
        LinearChart
    }
    
}
</script>

<style>


</style>