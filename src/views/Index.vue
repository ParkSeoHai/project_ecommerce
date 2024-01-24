<template>
    <!-- Home Slider -->
    <HomeSlider />
    <!-- Banner group -->
    <HomeBannerGroup />
    <!-- Section category -->
    <HomeCategory />
    <!-- Section flash sale -->
    <HomeFlashSale />
    <!-- Section collection -->
    <HomeCollectionGroup />
    <!-- Section Product group 1 -->
    <HomeCollectionListProduct
        :title="'iphone'"
        :linkUrl="'/listIphone'"
        :listIphone="listIphones"
    />
    <!-- Section home blog -->
    <HomeBlogNews />
</template>

<script setup>
import { ref } from 'vue';
// Component
import HomeSlider from '@/components/Home/HomeSlider.vue';
import HomeBannerGroup from '@/components/Home/HomeBannerGroup.vue';
import HomeCategory from '@/components/Home/HomeCategory.vue';
import HomeFlashSale from '@/components/Home/HomeFlashSale.vue';
import HomeCollectionGroup from '@/components/Home/HomeCollectionGroup.vue';
import HomeCollectionListProduct from '@/components/Home/HomeCollectionListProduct.vue';
import HomeBlogNews from '@/components/Home/HomeBlogNews.vue';

// List product
const listIphones = ref([
    { 
        id: 1,
        name: 'Đồng hồ thông minh XTF',
        image: 'src/assets/images/applewatch-4.jpg',
        colorCount: 5,
        price: '19,690,000₫',
        sale: '17,690,000₫'
    },
    { 
        id: 2,
        name: 'Đồng hồ thông minh XTF',
        image: 'src/assets/images/product-new-2.webp',
        colorCount: 5,
        price: '19,690,000₫',
        sale: '17,690,000₫'
    },
    { 
        id: 3,
        name: 'Đồng hồ thông minh XTF',
        image: 'src/assets/images/applewatch-4.jpg',
        colorCount: 5,
        price: '19,690,000₫',
        sale: '17,690,000₫'
    },
    { 
        id: 4,
        name: 'Đồng hồ thông minh XTF',
        image: 'src/assets/images/product-new-2.webp',
        colorCount: 5,
        price: '19,690,000₫',
        sale: '17,690,000₫'
    },
    { 
        id: 5,
        name: 'Đồng hồ thông minh XTF',
        image: 'src/assets/images/applewatch-4.jpg',
        colorCount: 5,
        price: '19,690,000₫',
        sale: '17,690,000₫'
    },
    { 
        id: 6,
        name: 'Đồng hồ thông minh XTF',
        image: 'src/assets/images/product-new-2.webp',
        colorCount: 5,
        price: '19,690,000₫',
        sale: '17,690,000₫'
    },
    { 
        id: 7,
        name: 'Đồng hồ thông minh XTF',
        image: 'src/assets/images/applewatch-4.jpg',
        colorCount: 5,
        price: '19,690,000₫',
        sale: '17,690,000₫'
    },
    { 
        id: 8,
        name: 'Đồng hồ thông minh XTF',
        image: 'src/assets/images/product-new-2.webp',
        colorCount: 5,
        price: '19,690,000₫',
        sale: '17,690,000₫'
    },
    { 
        id: 9,
        name: 'Đồng hồ thông minh XTF',
        image: 'src/assets/images/applewatch-4.jpg',
        colorCount: 5,
        price: '19,690,000₫',
        sale: '17,690,000₫'
    },
    { 
        id: 10,
        name: 'Đồng hồ thông minh XTF',
        image: 'src/assets/images/product-new-2.webp',
        colorCount: 5,
        price: '19,690,000₫',
        sale: '17,690,000₫'
    }
]);
</script>
