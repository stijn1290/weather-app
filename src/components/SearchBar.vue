<script setup>

import {ref} from "vue";
import axios from "axios";

let place = ref("");
const searchPlace = async () => {
  try {
    const res = await axios.get("https://geocoding-api.open-meteo.com/v1/search?name=" + place.value);
    emit("location", place.value);
  } catch (error) {
    console.log(error);
  }
}
const emit = defineEmits([
  "location",
])
</script>

<template>
  <form class="flex flex-row gap-2" @submit.prevent="searchPlace">
    <input v-model="place" type="text" id="searchIcon" class="bg-gray-700 text-gray-400 rounded-lg p-2 pl-10 pr-46 "
           placeholder="Search for a place...">
    <input @click="searchPlace" type="submit" value="Search" class="bg-blue-600 text-white rounded-lg p-2 px-4 cursor-pointer"/>
  </form>
</template>
