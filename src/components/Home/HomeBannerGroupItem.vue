<template>
    <div class="col-4 pe-0">
        <a href="#">
            <img :src="imageUrl" alt="" class="banner-group-img">
        </a>
    </div>
</template>

<script setup>

// Props import from Home/HomebannerGroup.vue
const { imageUrl } = defineProps(['imageUrl']);

</script>