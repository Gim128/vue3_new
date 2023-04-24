<template>
    <div>
        <p>No Reviews yet</p>
        <div class="reviewList">
            <ReviewItem 
                v-for="(item, i) in store.reviewsContent" 
                :key="i"
                :item="item"
            />
        </div>
    </div>
</template>

<script setup>
import ReviewItem from './ReviewItem.vue';
import { useReviewStore } from "../stores/review";

const store = useReviewStore();

</script>

<style lang="scss" scoped>

</style>