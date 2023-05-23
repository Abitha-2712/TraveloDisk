<template>
    <v-container>
      <v-card
      class="mx-auto"
      max-width="400"
      >
      <h3 class="text-h6 text-center " style="padding:5%;">User Registration</h3>
      <v-container style="width: 90%;">
        <v-text-field
          v-model="first"
          color="primary"
          label="First name"
          variant="underlined">
        </v-text-field>
  
        <v-text-field
          v-model="last"
          color="primary"
          label="Last name"
          variant="underlined">
        </v-text-field>
  
        <v-text-field
          v-model="email"
          color="primary"
          label="Email"
          variant="underlined">
        </v-text-field>
  
        <v-text-field
           v-model="password"
           name=" password"
           label="Password"
           type="password"
           placeholder="password"
           required>
       </v-text-field>
       <v-text-field
           v-model="password"
           name=" password"
           label="Confrim Password"
           type="password"
           placeholder="password"
           required>
       </v-text-field>
  
        <v-checkbox
          v-model="terms"
          color="blue"
          label="I agree to site terms and conditions">
        </v-checkbox>
      </v-container>
  
      <v-divider></v-divider>
  
      <v-card-actions>
        <v-spacer></v-spacer>
  
        <v-btn text color="black" block to="/loginpage">
          Register
  
          <v-icon icon="mdi-chevron-right" end></v-icon>
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-container>
  </template>
  
  <script >
  export default {
  
  }
  </script>
  
  <style>
  
  </style>