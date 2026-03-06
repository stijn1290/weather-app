<script setup>
import {computed} from "vue";

const props = defineProps({
  date: String,
  temperature_max: Number,
  temperature_min: Number,
})
const getWeekday = computed(() => {
  const date = new Date(props.date);
  return date.toLocaleDateString("en-US", {
    weekday: "long"
  });
});
</script>

<template>
  <div class="bg-gray-700 text-gray-400 rounded-lg p-4 flex flex-row justify-between gap-4 items-center">
    <h2 class="text-white text-center">{{ getWeekday }}</h2>
    <div class="flex flex-row gap-6">
      <img src="../../public/images/icon-drizzle.webp" alt="icon" class="h-12">
      <div class="flex flex-col justify-between">
        <h2>{{ temperature_min }}°</h2>
        <h2>{{ temperature_max }}°</h2>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>