<template>
    <div class="flash-sale-body list-product">
        <!-- Item -->
        <HomeFlashSaleBodyItem
            :imageUrl="'src/assets/images/applewatch-2.jpg'"
            :productName="'Đồng hồ thông minh XTF'"
            :colorCount="'5'"
            :productPrice="'7,950,000₫'"
            :productSale="'4,875,500₫'"
            :quantity="'26'"
            :percent="'60%'"
        />

        <!-- Item -->
        <HomeFlashSaleBodyItem
            :imageUrl="'src/assets/images/flashsale-product-3.webp'"
            :productName="'iPhone 14 Pro Max Chính hãng VNA'"
            :colorCount="'5'"
            :productPrice="'19,690,000₫'"
            :productSale="'17,524,100₫'"
            :quantity="'11'"
            :percent="'11%'"
        />

        <!-- Item -->
        <HomeFlashSaleBodyItem
            :imageUrl="'src/assets/images/applewatch-4.jpg'"
            :productName="'Đồng hồ thông minh XTF'"
            :colorCount="'5'"
            :productPrice="'24,250,000₫'"
            :productSale="'21,582,500₫'"
            :quantity="'90'"
            :percent="'90%'"
        />

        <!-- Item -->
        <HomeFlashSaleBodyItem
            :imageUrl="'src/assets/images/flashsale-product-5.webp'"
            :productName="'Oppo Reno 7XR Pro Chính Hãng'"
            :colorCount="'2'"
            :productPrice="'7,550,000₫'"
            :productSale="'5,550,000₫'"
            :quantity="'30'"
            :percent="'30%'"
        />

        <!-- Item -->
        <HomeFlashSaleBodyItem
            :imageUrl="'src/assets/images/flashsale-product-5.webp'"
            :productName="'Oppo Reno 7XR Pro Chính Hãng'"
            :colorCount="'2'"
            :productPrice="'7,550,000₫'"
            :productSale="'5,550,000₫'"
            :quantity="'30'"
            :percent="'30%'"
        />
    </div>
</template>

<script setup>
import HomeFlashSaleBodyItem from './HomeFlashSaleBodyItem.vue';
</script>