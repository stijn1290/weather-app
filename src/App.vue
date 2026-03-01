<script setup>
import Logo from "./components/Logo.vue";
import SearchBar from "./components/SearchBar.vue";
import WeatherConditions from "./components/WeatherConditions.vue";
import {ref} from "vue";
const selectedPlace = ref("");
</script>

<template>
  <header class="flex justify-between mb-10">
    <Logo/>
  </header>
  <main class="flex flex-col gap-10">
    <h1 class="text-5xl text-white font-medium text-center">How's the sky looking today?</h1>
    <section class="flex flex-col justify-center items-center">
      <SearchBar @location="selectedPlace = $event" />
    </section>
    <section class="grid grid-cols-[0.8fr_0.5fr]">
      <WeatherConditions :location="selectedPlace" />
    </section>
  </main>
</template>
