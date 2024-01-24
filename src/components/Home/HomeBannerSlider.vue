<template>
    <div class="banner-slider">
        <a href="#" class="slider-link">
            <img :src="imageUrl" alt="">
        </a>
    </div>
</template>

<script setup>

// Props import from Home/HomeSlider.vue
const { imageUrl } = defineProps(['imageUrl']);
</script>