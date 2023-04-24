<template>
  <div class="home">
    <div class="container">
      <!-- review form -->
      <Reviewform />
      <!-- review stats -->
      <ReviewStats />
      <!-- review List -->
      <ReviewList />
    </div>
  </div>
</template>

<script setup>
import ReviewList from '../components/ReviewList.vue';
import ReviewStats from '../components/ReviewStats.vue';
import Reviewform from '../components/Reviewform.vue';


</script>
