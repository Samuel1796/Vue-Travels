<script setup>
import { ref } from 'vue';

const drawer = ref(false);
const loading = ref(false);
const tab = ref(null);
const items = ref(['Destination', 'Bookings', 'Hotels', 'Flight']);

const load = ()=>{
  loading.value = true
  setTimeout(()=> (loading.value = false),5000)
}

</script>

<template>
  <div id="app">
      <v-app-bar scroll-behavior=" elevate" >
        <v-row justify="space-between" align="center" no-gutters>
          <v-app-bar-nav-icon
            @click="drawer = !drawer"
            class="d-flex d-sm-none"
          ></v-app-bar-nav-icon>
          <v-avatar image="data:image/jpeg;base64,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" size="50"></v-avatar>
          <v-toolbar-title >Tinch</v-toolbar-title>
          <v-tabs
            v-model="tab"
            align-with-title
            class="d-none d-sm-flex"
          >
            <v-tabs-slider color="yellow"></v-tabs-slider>

            <v-tab v-for="item in items" :key="item">
              {{ item }}
            </v-tab>
            <v-tab append-icon="mdi-account-plus" :loading="loading" @click="load">
              Get Started
            </v-tab>
            
          </v-tabs>
        </v-row>
      </v-app-bar>
      <!-- Add a navigation bar -->
      <v-navigation-drawer v-model="drawer" height="auto" temporary>
        <v-list nav dense>
          <v-list-item-group>
          
            <v-list-item v-for="(item, index) in items" :key="index">
              <v-list-item-title @click="tab = index">
                {{ item }}
              </v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-btn block append-icon="mdi-account-plus" :loading="loading" @click="load">
                Get Started
              </v-btn>
          </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
      <!-- Navigation bar ends -->
      <v-content class="ma-5">
        <v-tabs-items v-model="tab" class="d-flex flex-column align-center">
          <v-tab-item v-for="item in items" :key="item">
            
          </v-tab-item>
        </v-tabs-items>
      </v-content>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Kalam:wght@300&display=swap');
  *{
    font-family: 'Kalam', cursive;
  }

</style>


