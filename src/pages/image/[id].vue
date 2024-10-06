<template>
  <v-row class="flex flex-column justify-center align-center">
    <h1 class="h3 header">Your QuickiePixie Masterpiece</h1>
    <v-row>
        <img :src="url" type="image/png"></img>
        <a class="" :href="url" download="quickiepixie.png">Download as PNG</a>
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

const BASE_URL = `${process.env.VUE_APP_BACKEND_URL}/image`;

const url = `${BASE_URL}/${imageId}`;
</script>

<script>
</script>