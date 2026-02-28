<script setup>
import Logo from "./components/Logo.vue";
import SearchBar from "./components/SearchBar.vue";
</script>

<template>
  <header class="flex justify-center items-center w-full">
    <Logo/>
  </header>
  <main class="flex flex-col justify-center items-center w-full gap-10">
    <h1 class="text-5xl text-white font-medium">How's the sky looking today?</h1>
    <section class="flex flex-row gap-2">
      <SearchBar/>
    </section>
  </main>
</template>
