<script setup lang="ts">
import Header from './layouts/Header.vue';
</script>

<template>
  <v-app>
    <Header />
    <v-main>
      <NuxtPage />
    </v-main>
    <v-app />
  </v-app>
</template>
