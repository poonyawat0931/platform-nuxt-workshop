<script setup>
import Picture from '~/components/Picture.vue';

const BASE_URL = 'https://66cd864f8ca9aa6c8ccaa5f8.mockapi.io';
const contents = ref([]);

onMounted(async () => {
  const response = await fetch(`${BASE_URL}/contents`);
  contents.value = await response.json();
});
</script>

<template>
  <v-container>
    <div>
      <Picture />
    </div>
    <v-row dense>
      <v-col v-for="content in contents" :key="content.id" cols="12" xl="2">
        <ContentCard :content="content" />
      </v-col>
    </v-row>
  </v-container>
</template>
