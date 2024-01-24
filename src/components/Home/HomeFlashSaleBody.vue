<template>
    <div class="flash-sale-body list-product">
        <!-- Item -->
        <HomeFlashSaleBodyItem
            v-for="product in listProduct"
            :key="product.id"
            :productObj="product"
        />
    </div>
</template>

<script setup>
import { ref } from 'vue';
import HomeFlashSaleBodyItem from './HomeFlashSaleBodyItem.vue';

const listProduct = ref([
    {
        id: 1,
        imageUrl: "src/assets/images/applewatch-2.jpg",
        productName: "Đồng hồ thông minh XTF",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "26",
        percent: "60%"
    },
    {
        id: 2,
        imageUrl: "src/assets/images/flashsale-product-3.webp",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "11",
        percent: "11%"
    },
    {
        id: 3,
        imageUrl: "src/assets/images/applewatch-4.jpg",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "90",
        percent: "90%"
    },
    {
        id: 4,
        imageUrl: "src/assets/images/applewatch-4.jpg",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "90",
        percent: "90%"
    },
    {
        id: 3,
        imageUrl: "src/assets/images/flashsale-product-5.webp",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "50",
        percent: "50%"
    }
]);

</script>