<script setup>

const date = new Date();
defineProps({
  location: String,
})
</script>

<template>
<div class="bg-blue-500 text-white rounded-lg p-4 py-16 flex flex-row justify-between items-center">
  <div>
    <h2 class="font-medium text-xl">{{ location }}, Country</h2>
    <h2 class="text-gray-200">{{ date.getDay() }}, {{ date.getMonth() + 1}} {{ date.getDate() }}, {{ date.getFullYear() }}</h2>
  </div>
  <div class="flex flex-row items-center gap-6">
    <img src="/images/icon-sunny.webp" alt="condition" class="max-w-32 max-h-18">
    <h2 class="font-medium text-5xl">0°</h2>
  </div>
</div>
</template>

<style scoped>

</style>