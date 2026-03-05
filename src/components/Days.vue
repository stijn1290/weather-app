<script setup>
import Day from "./Day.vue";
import {weekdays} from "../js/dateNotations.js";
import {computed} from "vue";

const props = defineProps({
  dailyObj: Object,
})
const daysDate = computed(() => props.dailyObj.daily.time || []);
const temperature_2m_max = computed(() => props.dailyObj.daily.temperature_2m_max || []);
const temperature_2m_min = computed(() => props.dailyObj.daily.temperature_2m_min || []);
</script>

<template>
  <div class="flex flex-row justify-around gap-4" >
    <Day v-for="(day, index) in weekdays" :date="daysDate[index]" :temperature_max="temperature_2m_max[index]"
         :temperature_min="temperature_2m_min[index]"/>
  </div>
</template>

<style scoped>

</style>