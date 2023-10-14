<script setup>
import NavBar from './components/NavBar.vue'
import HomeComponent from './components/HomeComponent.vue'
// eslint-disable-next-line no-unused-vars
import { RouterView } from 'vue-router'
</script>

<template>
  <NavBar />

  <!-- <RouterView /> -->
  <home-component />
</template>

<style scoped>
@media (min-width: 1024px) {

}
</style>
