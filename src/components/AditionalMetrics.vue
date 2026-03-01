<script setup lang="ts">

import Metric from "./Metric.vue";
defineProps({
  feelsLike: String,
  humidity: String,
  windSpeed: String,
  precipitation: String,
})
</script>

<template>
  <div class="grid grid-cols-4 gap-4">
    <Metric :title="'Feels Like'" :stat="feelsLike + '°'"/>
    <Metric :title="'Humidity'" :stat="humidity + '%'"/>
    <Metric :title="'Wind'" :stat="windSpeed + 'km/h'"/>
    <Metric :title="'Precipitation'" :stat="precipitation + 'mm'"/>
  </div>
</template>

<style scoped>

</style>