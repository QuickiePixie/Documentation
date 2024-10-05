<template>
  <v-app>
    <v-main class="px-10 py-10">
      <AppHeader/>
      <div class="main">
        <router-view />
      </div>
      <AppFooter/>
    </v-main>
  </v-app>
</template>

<script setup>
  //
</script>

<style>
  .main {
    margin: auto;
    max-width: 1000px;
  }
</style>