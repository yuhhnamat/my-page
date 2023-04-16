<template>
  <div class="what-i-do pl-14">
    <p class="text-4xl">What I Do</p>
    <v-divider :thickness="4" class="border-opacity-75 w-1/3" color="success"></v-divider>
    <v-container>
      <v-row no-gutters>
        <v-col cols="12" sm="8">
          <bullet-point
            class="pl-8"
            v-for="(item, index) in jobs"
            :key="index"
            :bullet-point="item"
          />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script setup lang="ts">
import { getJobs } from '../composables/getJobs.ts'
import BulletPoint from './BulletPoint.vue'
const jobs = getJobs()
</script>

<style scoped></style>
