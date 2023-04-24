<template>
    <CardComponent>
        <button class="close">
            <i class="fa-sharp fa-solid fa-xmark"></i>
        </button>
        <button class="edit">
            <i class="fa-solid fa-pen-to-square" @click="store.editReview(item)"></i>

            <!-- 1:20:25 -->
        </button>
        <div class="num-display">
            {{ item.rating }}
        </div>
        <div class="text-display">
           {{ item.text }}
        </div>
    </CardComponent>
</template>

<script setup>
    import CardComponent from './CardComponent.vue';
    import { defineProps } from 'vue';
    import { useReviewStore } from "../stores/review";

    const store = useReviewStore();

    defineProps({
        item: {
            type: Object,
        }
    })
</script>

<style lang="scss" scoped>

</style>