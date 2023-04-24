<template>
    <CardComponent>
        <button class="close">
            <i class="fa-sharp fa-solid fa-xmark"></i>
        </button>
        <button class="edit">
            <i class="fa-solid fa-pen-to-square" @click="editReview(item)"></i>
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

    defineProps({
        item: {
            type: Object,
        }
    })
</script>

<style lang=