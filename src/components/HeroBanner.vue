<template>
  <div class="flex flex-row gap-8 justify-start pl-24 pt-16 pb-16">
    <v-avatar color="surface-variant" size="250px"></v-avatar>
    <div class="flex flex-col justify-center gap-x-4 gap-y-3">
      <p class="text-gray-400">{{ props.user.title }}</p>
      <p class="text-gray-600 font-sans text-5xl">{{ props.user.name }}</p>
      <p>{{ props.user.about }}</p>
      <div class="grid grid-cols-2 gap-4">
        <v-btn block rounded="xl">Resume</v-btn>
        <v-btn block rounded="xl">Contact</v-btn>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  user: {
    title: string
    name: string
    about: string
  }
}>()
</script>

<style scoped></style>
