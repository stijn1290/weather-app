<script setup>

const date = new Date();
</script>

<template>
<div class="bg-blue-500 text-white rounded-lg p-2 pl-10 pr-46 ">
  <h2>{{ date.getDay() }}, {{ date.getMonth() + 1}} {{ date.getDate() }}, {{ date.getFullYear() }}</h2>
</div>
</template>

<style scoped>

</style>