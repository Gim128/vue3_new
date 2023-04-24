<template>
    <div class="card" :class="{reverse: reverse}">
        <slot />
    </div>
</template>

<script>
    export default {
        name:"CardComponent",
        props: {
            reverse: {
                type: Boolean,
                default: false,
            }
        }
    }
</script>

<style scoped>
    .card{
        background: #ffffff;
        color: #212121;
    }

    .card.reverse {
        background: #212121;
        color: #ffffff;
    }
</style>