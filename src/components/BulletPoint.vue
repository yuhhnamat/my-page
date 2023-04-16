<template>
  <v-sheet>
    <v-container fluid>
      <div class="flex flex-row gap-x-6 w-8/12">
        <v-icon end :icon="iconName" size="x-large" />
        <div class="flex flex-col gap-y-1">
          <p class="text-xl">{{ props.bulletPoint.title }}</p>
          <p>{{ props.bulletPoint.content }}</p>
        </div>
      </div>
    </v-container>
  </v-sheet>
</template>
<script setup lang="ts">
import { computed } from 'vue'
const props = defineProps<{
  bulletPoint: {
    title: string
    icon: string
    content: string
  }
}>()
const iconName = computed(() => `mdi-${props.bulletPoint.icon}`)
</script>

<style scoped></style>
