<script setup lang="ts">

import Metric from "./Metric.vue";
</script>

<template>
  <div class="grid grid-cols-4 gap-4">
    <Metric :title="'Feels Like'" :stat="'°'"/>
    <Metric :title="'Humidity'" :stat="'%'"/>
    <Metric :title="'Wind'" :stat="'km/h'"/>
    <Metric :title="'Precipitation'" :stat="'mm'"/>
  </div>
</template>

<style scoped>

</style>