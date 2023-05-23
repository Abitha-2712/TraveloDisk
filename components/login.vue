<template>
  
  <v-container fluid fill-height>
     <v-layout align-center justify-center>
        <v-flex xs12 sm8 md4>
            <v-card class="mx-auto" max-width="400">
              <h3 class="text-h6 text-center " style="padding:5%;">User Login</h3>
            <v-card-text>
              <form ref="form" @submit.prevent="login()">
                     <v-text-field
                       v-model="username"
                       name="username"
                       label="Username"
                       type="text"
                       placeholder="username"
                       required
                    ></v-text-field>
                    
                     <v-text-field
                       v-model="password"
                       name="password"
                       label="Password"
                       type="password"
                       placeholder="password"
                       required
                    ></v-text-field>
                    
                    <v-card-actions>
<v-spacer></v-spacer>
<v-row>
<v-col> 
<v-btn text color="black" block to="/profilepage">
     login
</v-btn>
</v-col>
<v-col>
<v-btn text color="black" block to="/userpage">
Register

<v-icon icon="mdi-chevron-right" end></v-icon>
</v-btn>
</v-col>
</v-row>




</v-card-actions>
               </form>
              </v-card-text>
           </v-card>
         
        </v-flex>
     </v-layout>
  </v-container>

</template>

<script>
export default {
name: "Login",
data() {
return {
username: "",
password: "",
};
},
methods: {
login() {
const { username } = this;
console.log(username + "logged in")
},
},
};
</script>