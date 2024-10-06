<template>
    <v-row class="flex flex-column justify-center align-center">
        <h1 class="h1 header">About Us</h1>
    </v-row>
    <v-row class="flex-column align-left" v-for="member in data.team">
        <h4>{{ member.name }}</h4>
        <p>{{ member.desc }}</p>
    </v-row>
</template>

<script setup>
  //
  const data = {
    team: [
        {
            name: "Chelsea Chan",
            desc: ""
        },
        {
            name: "Rachel Kwan",
            desc: ""
        },
                {
            name: "Christine Zhao",
            desc: ""
        },
        {
            name: "Madison Majarais",
            desc: ""
        }
    ]
  }
</script>