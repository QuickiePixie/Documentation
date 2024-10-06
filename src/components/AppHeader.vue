<template>
  <v-row class="mx-5 my-5 font-weight-bold align-center">
    <img src="../assets\logo128.png" width="50"/>
    <nav>
        <RouterLink class="text-secondary" to="/">Home</RouterLink>
        <RouterLink class="text-secondary" to="/canvas">Draw</RouterLink>
        <RouterLink class="text-secondary" to="/about">About</RouterLink>
    </nav>
  </v-row>
</template>

<style>
    nav a {
        margin: 1rem;
        text-decoration: none;
        font-size: 1.2rem;
    }
</style>