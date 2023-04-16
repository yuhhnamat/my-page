<template>
  <main>
    <div class="flex flex-col gap-y-14 justify-center">
      <hero-banner :user="user" />
      <what-i-do />
      <my-projects />
      <fun-fact />
    </div>
  </main>
</template>

<script setup lang="ts">
import HeroBanner from '../components/HeroBanner.vue'
import WhatIDo from '../components/WhatIDo.vue'
import FunFact from '../components/FunFact.vue'
import MyProjects from '../components/MyProjects.vue'

import { getUser } from '../composables/getUser.ts'
const user = getUser()
</script>
