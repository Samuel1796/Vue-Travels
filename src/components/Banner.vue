<script setup lang="ts">
import { ref } from 'vue';
import { onMounted } from "vue";
import AOS from "aos";

onMounted(() => {
    AOS.init();
})

const loading = ref(false);
const load = ()=>{
  loading.value = true
  setTimeout(()=> (loading.value = false),5000)
}
</script>

<template>
  <div  class="d-flex flex-column flex-md-row">
    <div data-aos="fade-right" data-aos-duration="2000" class="pa-2 text-container">
      <p style="margin-top: 20%;">Best Destinations around the world</p>
      <h1 class="mb-4">Travel, Enjoy, and Live a New and Full Life</h1>
      <p class="text-h6 font-weight-light">Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam, veniam amet aspernatur libero nam fugit.</p>
      <v-btn size="large" append-icon="mdi-account-plus" :loading="loading" @click="load" style="margin-top: 5%;">Get Started</v-btn>
      <v-btn prepend-icon="mdi-play-circle-outline" variant="text" style="margin-top: 5%; margin-left:5%" size="large">Play Video</v-btn>
    </div>
    <div class="pa-5 image-container" style="margin-top: 0%;">
      <v-img src="../assets/img1.jpg" aspect-ratio="1" contain></v-img>
    </div>
  </div>

  <div  class="text-center mt-8" >
    <p>Category</p>
    <h1 class="mb-4 ">We Offer Best Services</h1>
  </div>

  <div class="d-flex flex-wrap justify-space-between px-4 ">
    <v-card data-aos="fade-right" data-aos-offset="300"
    data-aos-easing="ease-in-sine" data-aos-duration="1000"
     class="mx-auto pa-4 mb-4" max-width="300" tile :elevation="12">
      <v-icon class="icon" size="64">mdi-weather-hail</v-icon>
      <v-card-title class="text-center mt-2">Calculated Weather</v-card-title>
      <v-card-text class="text-center">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</v-card-text>
    </v-card>

    <v-card data-aos="fade-up" data-aos-offset="300"
    data-aos-easing="ease-in-sine" data-aos-duration="1000"
     class="mx-auto pa-4 mb-4" max-width="300" tile :elevation="12">
      <v-icon class="icon" size="64">mdi-airplane</v-icon>
      <v-card-title class="text-center mt-2">Flights</v-card-title>
      <v-card-text class="text-center">Sed ut perspiciatis unde omnis iste natus error sit voluptatem.</v-card-text>
    </v-card>

    <v-card data-aos="fade-down" data-aos-offset="300"
    data-aos-easing="ease-in-sine" data-aos-duration="1000"
     class="mx-auto pa-4 mb-4" max-width="300" tile :elevation="12">
      <v-icon class="icon" size="64">mdi-briefcase</v-icon>
      <v-card-title class="text-center mt-2">Jobs</v-card-title>
      <v-card-text class="text-center">At vero eos et accusamus et iusto odio dignissimos ducimus.</v-card-text>
    </v-card>

    <v-card data-aos="fade-left" data-aos-offset="300"
    data-aos-easing="ease-in-sine" data-aos-duration="1000"
     class="mx-auto pa-4 mb-4" max-width="300" tile :elevation="12">
      <v-icon class="icon" size="64">mdi-walk</v-icon>
      <v-card-title class="text-center mt-2">Shopping</v-card-title>
      <v-card-text class="text-center">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</v-card-text>
    </v-card>
  </div>


  <!-- Destinations -->
  <div class="text-center mt-14">
    <p>Top Selling</p>
    <h1 class="mb-4"> Top Destinations</h1>
  </div>

  <div class="d-flex justify-center flex-wrap">
    <v-col cols="12" md="4">
      <v-card data-aos="flip-left" data-aos-duration="1000"
       class="mx-auto" max-width="400" outlined rounded>
        <v-img src="https://heyexplorer.com/wp-content/uploads/2022/05/kyoto-japan-street-1024x684.jpg" height="300"></v-img>
        <v-card-title class="text-h5">
          <span style="color: blue;">JAPAN</span>
        </v-card-title>
        <v-card-text>
          <p><v-icon>mdi-send</v-icon>10 days trip</p>
        </v-card-text>
      </v-card>
    </v-col>
    <v-col cols="12" md="4">
      <v-card v-card data-aos="flip-left" data-aos-duration="1500"
       class="mx-auto" max-width="400" outlined rounded>
        <v-img src="https://assets3.thrillist.com/v1/image/2875152/1584x1056/crop;jpeg_quality=60;progressive.jpg" height="300"></v-img>
        <v-card-title class="text-h5">
          <span style="color: blue;">AUSTRALIA</span>
        </v-card-title>
        <v-card-text>
          <p><v-icon>mdi-send</v-icon> 2 days trip</p>
        </v-card-text>
      </v-card>
    </v-col>
    <v-col cols="12" md="4">
      <v-card v-card data-aos="flip-left" data-aos-duration="2000"
       class="mx-auto" max-width="400" outlined rounded>
        <v-img src="https://kawa-news.com/wp-content/uploads/2022/06/bigstock-RIYADH-FEBRUARY-Aerial-v-133739978-820x500.jpg" height="300"></v-img>
        <v-card-title class="text-h5">
          <span style="color: blue;">SAUDI ARABIA</span>
        </v-card-title>
        <v-card-text>
          <p><v-icon>mdi-send</v-icon>29 days trip</p>
        </v-card-text>
      </v-card>
    </v-col>
  </div>

  <!-- Steps -->
  <div class="d-flex flex-wrap" style="margin-top: 5%">
    <div class="col-md-8 p-4" style="padding-left: 10%;">
      <!-- Left container with 2/3 width -->
      <p class="">Easy and Fast</p>
      <h1 class="mb-4  font-weight-black">Book Your Next Trip In 3 Easy Steps</h1>
    
      <v-spacer></v-spacer>
      <!-- 1st row -->
      <div data-aos="fade-up-right" data-aos-duration="1000"
      class="d-flex align-items-center mb-3" style="margin-top: 5%;">
        <img src="https://cdn.pixabay.com/photo/2017/01/10/03/54/icon-1968240_640.png" alt="Image 1" width="60" height="60" class="mr-3">
        <div>
          <h1 class=" mb-1">Choose Your Destination</h1>
          <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
      </div>
    
      <!-- 2nd row -->
      <div data-aos="fade-up-right" data-aos-duration="2000"
       class="d-flex align-items-center mb-3" style="margin-top: 5%;">
        <img src="https://img.freepik.com/free-vector/nfc-technology-concept-illustration_114360-14387.jpg?size=626&ext=jpg" alt="Image 2" width="60" height="60" class="mr-3">
        <div>
          <h1 class=" mb-1">Make Payment</h1>
          <p class="text-muted">Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        </div>
      </div>
    
      <!-- 3rd row -->
      <div data-aos="fade-up-right" data-aos-duration="3000" 
       class="d-flex align-items-center mb-3" style="margin-top: 5%;">
        <img src="https://img.freepik.com/free-icon/airplane_318-416026.jpg?size=626&ext=jpg" alt="Image 3" width="60" height="60" class="mr-3">
        <div>
          <h1 class=" mb-1">Reach Airport on Selected Dates</h1>
          <p class="text-muted">Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi<br/> ut aliquip ex ea commodo consequat.</p>
        </div>
      </div>
    </div>
    
    <div class="col-md-4 p-4" style="padding-left: 10%;">
      <!-- Right container with 1/3 width -->

  
        <v-card
          class="mx-auto my-12"
          width="350"
          data-aos="zoom-in-left" data-aos-duration="2000"
        >
          <v-img
            cover
            height="250"
            src="https://santorinidave.com/wp-content/uploads/2023/01/san-francisco-where-to-stay-golden-gate-bridge.jpeg"
          ></v-img>
      
          <v-card-item>
            <v-card-title>Trip to San Francisco</v-card-title>
      
            <v-card-subtitle>
              <span class="me-1">Alcatraz</span>
      
              <v-icon
                color="error"
                icon="mdi-fire-circle"
                size="small"
              ></v-icon>
            </v-card-subtitle>
          </v-card-item>
      
          <v-card-text>
            <v-row
              align="center"
              class="mx-0"
            >
              <v-rating
                :model-value="4.5"
                color="amber"
                density="compact"
                half-increments
                readonly
                size="small"
              ></v-rating>
      
              <div class="text-grey ms-4">
                4.5 (413)
              </div>
            </v-row>
      
            <div class="my-4 text-subtitle-1">
              <h2>$450 • American, History</h2>
            </div>
      
            <div>31st July,2023</div>
          </v-card-text>
      
          <v-card-actions>
            <v-btn
              color="deep-purple-lighten-2"
              variant="text"
              :loading="loading" @click="load"
            >
              Book
            </v-btn>
          </v-card-actions>
        </v-card>
       </div>
  </div>

  <!-- Company -->

  <v-container data-aos="zoom-out-up" fluid style="margin-bottom:5%;" >
    <v-row justify="center" >
      <v-col cols="6" sm="4" md="2">
        <v-card class="d-flex align-center justify-center pa-1">
          <v-img src="https://logos-world.net/wp-content/uploads/2023/01/Jetstar-Logo-500x281.png" width="80" height="80" contain></v-img>
        </v-card>
      </v-col>
      <v-col cols="6" sm="4" md="2">
        <v-card class="d-flex align-center justify-center pa-1">
          <v-img src="https://logos-world.net/wp-content/uploads/2021/02/British-Airways-Logo-700x394.png" width="80" height="80" contain></v-img>
        </v-card>
      </v-col>
      <v-col cols="6" sm="4" md="2">
        <v-card class="d-flex align-center justify-center pa-1">
          <v-img src="https://logos-world.net/wp-content/uploads/2020/03/Qatar-Airways-Logo-700x394.png" width="80" height="80" contain></v-img>
        </v-card>
      </v-col>
      <v-col cols="6" sm="4" md="2">
        <v-card class="d-flex align-center justify-center pa-1">
          <v-img src="https://logos-world.net/wp-content/uploads/2021/05/Air-Canada-Logo-700x394.png" width="80" height="80" contain></v-img>
        </v-card>
      </v-col>
    </v-row>
  </v-container>

  <!-- Subscribe -->
  <div class="pb-12">
  <v-container fluid class=" px-0" 
   style="background: linear-gradient(to bottom right, #f8bbd0, #d1c4e9);
        max-width:100%; height: auto;">
    <v-row class="d-flex justify-center align-center" no-gutters>
      <v-col cols="12" sm="8" md="6">
        <h2 class="text-center font-weight-bold px-2">Subscribe to Our Newsletter</h2>
        <v-form>
          <v-row>
            <v-col cols="12">
              <v-text-field label="Email Address" outlined dense></v-text-field>
            </v-col>
            <v-col cols="12" class="text-center">
              <v-btn color="primary" class="white--text" outlined large rounded 
              data-aos="zoom-in-down" data-aos-duration="1500">
                Subscribe
              </v-btn>
            </v-col>
          </v-row>
        </v-form>
      </v-col>
    </v-row>
  </v-container>
</div>


</template>

  
  <style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Kalam:wght@300&display=swap');
  *{
    font-family: 'Kalam', cursive;
  }
  .text-container {
    flex: 1;
    height: 100%;
  }
  
  .image-container {
    display: none;
    flex: 2;
  }
  
  @media (min-width: 768px) {
    .text-container {
      flex: 2;
    }
  
    .image-container {
      display: block;
    }
  }
  .icon {
    display: block;
    margin: 0 auto;
  }
  
  
  </style>
  