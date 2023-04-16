<template>
  <v-card hover="true" variant="outlined" class="mx-4 w-60">
    <v-card-title> <v-icon size="x-large" end :icon="iconName" /> </v-card-title>

    <v-card-subtitle>
      <div class="gap-y-10">
        <p class="text-gray-600 text-2xl flex-wrap">{{ props.title }}</p>
        <p class="text-gray-400 text-4xl">{{ props.content }}</p>
      </div>
    </v-card-subtitle>
  </v-card>
</template>

<script setup lang="ts">
import { computed } from 'vue'
const props = defineProps<{
  title: string
  icon: string
  content: string
}>()
const iconName = computed(() => `mdi-${props.icon}`)
</script>

<style scoped></style>
