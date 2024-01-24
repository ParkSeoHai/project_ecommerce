<template>
    <!-- Banner group -->
    <section id="banner-group">
        <div class="container p-0">
            <div class="bg-color-white">
                <div class="row">
                    <!-- Item -->
                    <HomeBannerGroupItem :imageUrl="'src/assets/images/banner-group-1.webp'" />
                    <HomeBannerGroupItem :imageUrl="'src/assets/images/banner-group-2.webp'" />
                    <HomeBannerGroupItem :imageUrl="'src/assets/images/banner-group-3.webp'" />
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import HomeBannerGroupItem from './HomeBannerGroupItem.vue';
</script>