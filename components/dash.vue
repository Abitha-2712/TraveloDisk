<template>
    <v-card
      class="mx-auto"
      max-width="400"
    >
      <v-list-item two-line>
        <v-list-item-content>
          <v-list-item-title class="text-h5">
            Car Ride
          </v-list-item-title>
          <v-list-item-subtitle>Mon, 9:30 AM,</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
  
      <v-card-text>
        <v-row align="center">
          <v-col
            class="text-h2"
            cols="6"
          >
            2 ride
          </v-col>
          <v-col cols="6">
            <v-img
              src="https://cars.tatamotors.com/images/dark/m-altroz-home.jpg"
              alt="Car image"
              width="150"
            ></v-img> 
          </v-col>
        </v-row>
      </v-card-text>
  
      <v-list-item>
        <v-list-item-icon>
          <v-icon>mdi-send</v-icon>
        </v-list-item-icon>
        <v-list-item-subtitle>23 km/h</v-list-item-subtitle>
      </v-list-item>
  
      <v-list-item>
        <v-list-item-icon>
          <v-icon>mdi-cloud-download</v-icon>
        </v-list-item-icon>
        <v-list-item-subtitle>48%</v-list-item-subtitle>
      </v-list-item>
  
      <v-slider
        v-model="time"
        :max="6"
        :tick-labels="labels"
        class="mx-4"
        ticks
      ></v-slider>
  
      <v-list class="transparent">
        <v-list-item
          v-for="item in forecast"
          :key="item.day"
        >
          <v-list-item-title>{{ item.day }}</v-list-item-title>
  
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
  
          <v-list-item-subtitle class="text-right">
            {{ item.temp }}
          </v-list-item-subtitle>
        </v-list-item>
      </v-list>
    <v-divider></v-divider>
      <v-card-actions>
        <v-btn text>
          Full Report
        </v-btn>
      </v-card-actions>
    </v-card>
  </template>
  <script>
    export default {
      data () {
        return {
          labels: ['SU', 'MO', 'TU', 'WED', 'TH', 'FR', 'SA'],
          time: 0,
          forecast: [
            { day: 'Tuesday', icon: 'mdi-car' },
            { day: 'Wednesday', icon: 'mdi-car' },
            { day: 'Thursday', icon: 'mdi-car' },
          ],
        }
      },
    }
  </script>