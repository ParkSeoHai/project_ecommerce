<template>
    <div class="banner-slider">
        <a href="#" class="slider-link">
            <img :src="imageUrl" alt="">
        </a>
    </div>
</template>

<script setup>
const { imageUrl } = defineProps(['imageUrl']);
</script>