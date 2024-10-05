<template>
  <v-row class="flex flex-column justify-center align-center">
    <h1 class="h1 header">QuickiePixie</h1>
    <h2 class="h2 subheader">Quick, Easy, Pixels</h2>

    <v-row class="flex mt-5">
        <h3>Try it out!</h3>
        <v-btn class="btn my-2 w-100" to="/canvas">Web Canvas</v-btn>
        <v-btn class="btn w-100">Adobe Express</v-btn>
    </v-row>
  </v-row>
</template>

<script setup>
  //
</script>

<style>
    .header {
        font-size: 5rem;
    }
</style>
