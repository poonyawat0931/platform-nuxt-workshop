<template>
    <v-card class="mx-auto" max-width="344">
        <v-img height="200px" :src="content.description" cover></v-img>

        <v-card-title>
            {{ content.name }}
        </v-card-title>

        <v-card-subtitle>
            {{ content.country }}
        </v-card-subtitle>

        <v-card-actions>
            <v-btn color="orange-lighten-2" text="Explore"></v-btn>

            <v-spacer></v-spacer>

            <v-btn :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="show = !show"></v-btn>
        </v-card-actions>

        <v-expand-transition>
            <div v-show="show">
                <v-divider></v-divider>
                <v-card-text>
                    Description: {{ content.description }}
                </v-card-text>
            </div>
        </v-expand-transition>
    </v-card>
</template>

<script setup>
import { ref } from 'vue';

const props = defineProps({
    content: Object
});

const show = ref(false);
</script>