<template>
    <img src="https://placehold.co/1200x800" alt="">
    <div class="description">
        <p class="number">{{ number }}</p>
        <p class="description__title">{{ title }}</p>
        <p class="description__content">{{ content }}</p>
    </div>
</template>

<script setup>
    import {defineProps} from 'vue'

    const props = defineProps({
        number: {
            type: String,
            required: false,
        },
        title: {
            type: String,
            required: false,
        },
        content: {
            type: String,
            required: false,
        },
    });
</script>