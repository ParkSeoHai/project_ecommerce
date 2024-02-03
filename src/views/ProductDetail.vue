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