<template>
  <div class="facts flex flex-col pl-14">
    <p class="text-4xl">Fun Facts</p>
    <v-divider :thickness="4" class="border-opacity-75 w-1/3" color="success"></v-divider>
    <div class="flex flex-row justify-center pt-8 pl-4">
      <fun-card
        v-for="(item, index) in cardContents"
        :key="index"
        :title="item.title"
        :icon="item.icon"
        :content="item.content"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import FunCard from './FunCard.vue'
const cardContents = [
  {
    title: 'Developer',
    icon: 'dev-to',
    content: '1'
  },
  {
    title: 'Coding Hours',
    icon: 'cards-heart-outline',
    content: '2000+'
  },
  {
    title: 'Commits',
    icon: 'source-commit',
    content: '500+'
  },
]
</script>

<style scoped></style>
