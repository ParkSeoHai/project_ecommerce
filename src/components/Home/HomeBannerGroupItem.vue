<template>
    <div class="col-4 pe-0">
        <a href="#">
            <img :src="imageUrl" alt="" class="banner-group-img">
        </a>
    </div>
</template>

<script setup>
const { imageUrl } = defineProps(['imageUrl']);

</script>