<template>
  <v-app>
  <v-navigation-drawer permanent>
          <v-list>
            <v-list-item class="px-2">
              <v-list-item-avatar size="40" color="grey lighten-2">
                  <img :src="userImage" alt="User avatar" @click="openFileSelector">
  <v-icon class="camera-icon" color="grey darken-1">mdi-camera</v-icon>
  <input type="file" ref="fileInput" style="display: none" @change="onFileSelected">
              </v-list-item-avatar>
            </v-list-item>
  
            <v-list-item link>
              <v-list-item-content>
                <v-list-item-title class="text-h6">
                  {{username || 'Username'}}
                </v-list-item-title>
                
              </v-list-item-content>
            </v-list-item>
          </v-list>
  
        <v-divider></v-divider>
  
        <v-list
          dense
          nav
        >
          <v-list-item
            v-for="item in items"
            :key="item.title"
            link
          >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
  
            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-divider></v-divider>
          <v-spacer></v-spacer>
          <v-btn text color="black" block to="/loginpage" >
           Logout
    </v-btn>
    <v-divider></v-divider>
          <v-spacer></v-spacer>
          <v-btn text color="black" block to="/dashboard" >
           Dashboard
    </v-btn>
        </v-list>
      </v-navigation-drawer>
  </v-app>
  </template>
  
  <script>
    export default {
      
   
data () {
        return {
          items: [
            { title: 'My Profile', icon: 'mdi-view-dashboard' },
            { title: 'My Trips', icon: 'mdi-car' },
            { title: 'Ride now', icon: 'mdi-bike' },
            { title: 'Help', icon: 'mdi-help-box' },
            { title: 'Home', icon: 'mdi-home-city' },
          ],
          username:this.$route.params.username
  
        }
      },
      methods: {
        logout() {
          this.$router.replace({name:'login'})
        }
      },
      
    }
  </script>