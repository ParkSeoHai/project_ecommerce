<template>
    <!-- Home Slider -->
    <section id="home-slider">
        <div class="container p-0">
            <div class="row">
                <div class="col-3">
                    <!-- Navbar -->
                    <Navbar />
                </div>
                <div class="col-9 pt-3 ps-0">
                    <HomeBannerSlider :imageUrl="'src/assets/images/banner-slider-1.webp'" />
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import Navbar from '../Navbar.vue';
import HomeBannerSlider from './HomeBannerSlider.vue';
</script>