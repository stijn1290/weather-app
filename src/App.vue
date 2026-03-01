<script setup>
import Logo from "./components/Logo.vue";
import SearchBar from "./components/SearchBar.vue";
import WeatherConditions from "./components/WeatherConditions.vue";
import {ref} from "vue";
import AditionalMetrics from "./components/AditionalMetrics.vue";
const selectedPlace = ref("");
const temperature = ref("");
const country = ref("");
const feelsLike = ref("");
const humidity = ref("");
const windSpeed = ref("");
const precipitation = ref("");
</script>

<template>
  <header class="flex justify-between mb-10">
    <Logo/>
  </header>
  <main class="flex flex-col gap-10">
    <h1 class="text-5xl text-white font-medium text-center">How's the sky looking today?</h1>
    <section class="flex flex-col justify-center items-center">
      <SearchBar @location="selectedPlace = $event" @temperature="temperature = $event"
                 @country="country = $event" @feelsLike="feelsLike = $event" @humidity="humidity = $event"
       @windSpeed="windSpeed = $event" @precipitation="precipitation = $event"/>
    </section>
    <section class="grid grid-cols-[0.8fr_0.5fr]">
      <div class="flex flex-col gap-10">
        <WeatherConditions :location="selectedPlace" :temperature="temperature" :country="country" />
        <AditionalMetrics :feelsLike="feelsLike" :humidity="humidity" :windSpeed="windSpeed" :precipitation="precipitation" />
      </div>
    </section>
  </main>
</template>
