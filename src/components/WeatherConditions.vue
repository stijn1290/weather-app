<script setup>
import {weekdays,months} from '../js/dateNotations.js';
const date = new Date();
defineProps({
  location: String,
  temperature: String,
  country: String,
})
</script>

<template>
<div class="bg-blue-600 text-white rounded-lg p-4 py-16 flex flex-row justify-between items-center">
  <div>
    <h2 class="font-medium text-xl">{{ location }}, {{ country }}</h2>
    <h2 class="text-gray-200">{{ weekdays[date.getDay()] }}, {{ months[date.getMonth()] }} {{ date.getDate() }},
      {{ date.getFullYear() }}</h2>
  </div>
  <div class="flex flex-row items-center gap-6">
    <img src="/images/icon-sunny.webp" alt="condition" class="max-w-32 max-h-18">
    <h2 class="font-medium text-5xl">{{ temperature }}°</h2>
  </div>
</div>
</template>

<style scoped>

</style>