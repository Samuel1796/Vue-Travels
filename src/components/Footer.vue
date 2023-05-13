<script setup lang="ts">
import { onMounted } from "vue";
import AOS from "aos";

onMounted(() => {
    AOS.init();
})

</script>

<template>
    <v-container fluid data-aos="fade-up"
    data-aos-duration="1500">
      <v-row class="py-8">
        <v-col cols="6" sm="4" md="3" class="text-center">
          <h3 class="mb-2 font-weight-bold">Allies</h3>
          <p class="mb-1">Fly Emirates</p>
          <p class="mb-1">Nimoslaw Travels</p>
          <p class="mb-1">Travel With Yakubu </p>
          <p class="mb-1">Hotel Oblivion </p>

        </v-col>
        <v-col cols="6" sm="4" md="3" class="text-center">
          <h3 class="mb-2 font-weight-bold">Contact Us</h3>
          <p class="mb-1">123 Main Street</p>
          <p class="mb-1">Western Region, Ghana</p>
          <p class="mb-1">Phone: (+233) 557272539</p>
          <p class="mb-1">Email: sboakye179@gmail.com</p>
        </v-col>
        <v-col cols="6" sm="4" md="3" class="text-center">
          <h3 class="mb-2 font-weight-bold">More</h3>
          <p class="mb-1">About Us</p>
          <p class="mb-1">Our Services</p>
          <p class="mb-1">Testimonials</p>
          <p class="mb-1">FAQs</p>
        </v-col>
        <v-col cols="6" sm="4" md="3" class="text-center">
          <h3 class="mb-2 font-weight-bold">Connect To Us</h3>
          <v-row>
            <v-col cols="2">
              <v-icon class="mx-auto" size="30">mdi-github</v-icon>
            </v-col>
            <v-col cols="2">
              <v-icon class="mx-auto" size="30">mdi-twitter</v-icon>
            </v-col>
            <v-col cols="2">
              <v-icon class="mx-auto" size="30">mdi-instagram</v-icon>
            </v-col>
            <v-col cols="2">
              <v-icon class="mx-auto" size="30">mdi-linkedin</v-icon>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <v-row class="mt-6">
        <v-col
          cols="12"
          class="text-center"
        >
          &copy; 2023 Boakye Samuel. All Rights Reserved.
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <style scoped>
    /* Add any custom styles here */
  @import url('https://fonts.googleapis.com/css2?family=Kalam:wght@300&display=swap');
  *{
    font-family: 'Kalam', cursive;
  }
  </style>
  