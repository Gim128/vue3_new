<template>
  <div>
    <HeaderComponent />
    <RouterView />
  </div>
</template>

<script setup>
import { RouterView } from 'vue-router'
import HeaderComponent from './components/HeaderComponent.vue';

</script>

<style scoped>

</style>
