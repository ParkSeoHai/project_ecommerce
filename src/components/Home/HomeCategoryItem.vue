<template>
    <div class="item">
        <div class="box-cat">
            <a href="#" class="link-img-cat">
                <div class="box-img">
                    <img
                        :src="props.imageUrl"
                        :alt="props.categoryName"
                    >
                </div>
                <span class="banner-content">{{ props.categoryName }}</span>
            </a>
        </div>
    </div>
</template>

<script setup>
const props = defineProps(['imageUrl', 'categoryName']);
</script>