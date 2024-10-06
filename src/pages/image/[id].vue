<template>
  <v-row class="flex flex-column justify-center align-center">
    <h1 class="h3 header">Your QuickiePixie Masterpiece</h1>
    <v-row>
        <img :src="url" type="image/png"></img>
    </v-row>
    <v-row>
      <a class="" :href="url" download="quickiepixie.png">Download as PNG</a>
    </v-row>
    <v-row class="h4 flex-column">
      <div class="my-4">To share your work of art, use the link below:</div>
      <h5>{{pageUrl}}</h5>
    </v-row>
  </v-row>
</template>

<script setup>
  //
import { useRoute } from 'vue-router'

const route = useRoute();
console.log(route);

const imageId = route.params.id;

console.log(imageId)

console.log(import.meta.env.VITE_API_URL)

const BASE_URL = `${import.meta.env.VITE_APP_BACKEND_URL}/image`;

const url = `${BASE_URL}/${imageId}`;

const pageUrl = `${import.meta.env.VITE_APP_FRONTEND_URL}/image/${imageId}`
</script>

<script>
</script>