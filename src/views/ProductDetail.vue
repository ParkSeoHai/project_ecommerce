<template>
    <!-- Breadcrumb -->
    <Breadcrumb
        :breadcrumbs="breadcrumbs"
        :breadcrumbActive="breadcrumbActive"
    />
    <!-- Product detail info -->
    <div id="product-template" class="product-page">
        <!-- Section product detail -->
        <ProductDetailInfo />

        <div class="row pt-4">
            <div class="col-9">
                <div class="bg-color-white"></div>
            </div>
            <div class="col-3">
                <div class="bg-color-white"></div>
            </div>
        </div>
    </div>
</template>

<script setup>
import Breadcrumb from '@/components/Breadcrumb.vue';
import ProductDetailInfo from '@/components/ProductDetail/ProductDetailInfo.vue';

// List breadcrumbs
let breadcrumbs = [
    {
        linkText: 'Trang chủ',
        linkUrl: '/home'
    },
    {
        linkText: 'Điện thoại',
        linkUrl: '/dienthoai'
    },
    {
        linkText: 'iPhone',
        linkUrl: '/iphone'
    },
    {
        linkText: 'iPhone 12 Series',
        linkUrl: '/iphone-12-series'
    }
];

let breadcrumbActive = 'iPhone 12 Chính hãng VN/A';
</script>