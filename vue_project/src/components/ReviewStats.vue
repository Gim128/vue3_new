<template>
    <div class="feedback-stats">
        {{ store.reviewsCount ? store.reviewsCount : "No" }}
        <h4>3 Reviews</h4>
        <h4>Average Rating: {{ isNaN(store.averageRating) ? 0 : store.averageRating }}</h4>
    </div>
</template>

<script setup>
import { useReviewStore } from "../stores/review";

const store = useReviewStore();
</script>

<style lang="scss" scoped>

</style>