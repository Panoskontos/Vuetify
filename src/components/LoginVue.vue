<template>
  <v-container>
     <v-card width="400px" class="mt-5 mx-a">
       <v-card-title>
        <h1>Login</h1>
      </v-card-title>
       <v-card-text>
        <v-form>
          <v-text-field label="Username"
           prepend-icon="mdi-account-circle"
          />
           <v-text-field 
            type="Password"
            label="Password" 
            prepend-icon="mdi-lock"
          />
        </v-form>
        <v-divider></v-divider>
         <v-card-actions>
        <v-btn color="success">Register</v-btn>
        <v-spacer></v-spacer>
        <v-btn color="info">Login</v-btn>
      </v-card-actions>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>


export default {
  name: 'LoginVue',
  data: () => ({
    //
  }),
}

</script>