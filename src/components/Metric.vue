<script setup>
defineProps({
  title: String,
  stat: String,
})
</script>

<template>
  <div class="bg-gray-700 text-gray-400 rounded-lg p-4 flex flex-col gap-4">
    <h2 class="font-medium text-lg">{{ title }}</h2>
    <h2 class="text-white text-xl">{{ stat }}</h2>
  </div>
</template>

<style scoped>

</style>