<template>
    <!-- Section flash sale -->
    <section id="section-flash-sale">
        <div class="container p-0">
            <div class="bg-flash-sale">
                <!-- Top -->
                <HomeFlashSaleTop />
                <!-- Body -->
                <HomeFlashSaleBody />
                <!-- Bottom -->
                <HomeFlashSaleBottom />
            </div>
        </div>
    </section>
</template>

<script setup>
import HomeFlashSaleTop from './HomeFlashSaleTop.vue';
import HomeFlashSaleBody from './HomeFlashSaleBody.vue';
import HomeFlashSaleBottom from './HomeFlashSaleBottom.vue';
</script>