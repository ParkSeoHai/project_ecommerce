<template>
    <div class="flash-sale-body">
        <button
            v-if="circleCount > 1"
            class="btn-arrow btn-arrow-left"
            @click.prevent="handleArrowProduct(1)"
        >
            <i class="bi bi-chevron-compact-left"></i>
        </button>
        <div class="block-body">
            <div 
                class="list-product"
                :style="[
                    `grid-template-columns: repeat(${listProduct.length}, 1fr)`,
                    `width: ${widthListProduct}px`,
                    `margin-left: ${marginLeft}px`
                ]"
            >
                <!-- Item -->
                    <HomeFlashSaleBodyItem
                    v-for="product in listProduct"
                    :key="product.id"
                    :productObj="product"
                />
            </div>
            <ul
                v-if="circleCount > 1"
                class="list-circle"
            >
                <li class="item"
                    v-for="n in circleCount"
                    :key="n"
                    :class="(n - 1) * -widthBlog === marginLeft ? 'active' : ''"
                    @click.prevent="handleCircleProduct(n - 1)"
                ></li>
            </ul>
        </div>
        <button
            v-if="circleCount > 1"
            class="btn-arrow btn-arrow-right"
            @click.prevent="handleArrowProduct(-1)"
        >
            <i class="bi bi-chevron-compact-right"></i>
        </button>
    </div>
</template>

<script setup>
import { ref } from 'vue';
// Component
import HomeFlashSaleBodyItem from './HomeFlashSaleBodyItem.vue';

const listProduct = ref([
    {
        id: 1,
        imageUrl: "src/assets/images/applewatch-2.jpg",
        productName: "Đồng hồ thông minh XTF",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "1",
        percent: "60%"
    },
    {
        id: 2,
        imageUrl: "src/assets/images/flashsale-product-3.webp",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "2",
        percent: "11%"
    },
    {
        id: 3,
        imageUrl: "src/assets/images/applewatch-4.jpg",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "3",
        percent: "90%"
    },
    {
        id: 4,
        imageUrl: "src/assets/images/applewatch-4.jpg",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "4",
        percent: "90%"
    },
    {
        id: 5,
        imageUrl: "src/assets/images/flashsale-product-5.webp",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "5",
        percent: "50%"
    },
    {
        id: 1,
        imageUrl: "src/assets/images/applewatch-2.jpg",
        productName: "Đồng hồ thông minh XTF",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "6",
        percent: "60%"
    },
    {
        id: 2,
        imageUrl: "src/assets/images/flashsale-product-3.webp",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "7",
        percent: "11%"
    },
    {
        id: 3,
        imageUrl: "src/assets/images/applewatch-4.jpg",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "8",
        percent: "90%"
    }
    ,
    {
        id: 2,
        imageUrl: "src/assets/images/flashsale-product-3.webp",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "9",
        percent: "11%"
    },
    {
        id: 2,
        imageUrl: "src/assets/images/flashsale-product-3.webp",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "10",
        percent: "11%"
    },
    {
        id: 3,
        imageUrl: "src/assets/images/applewatch-4.jpg",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "11",
        percent: "90%"
    }
    ,
    {
        id: 2,
        imageUrl: "src/assets/images/flashsale-product-3.webp",
        productName: "iPhone 14 Pro Max Chính hãng VNA",
        colorCount: 5,
        productPrice: "7,950,000₫",
        productSale: "4,875,500₫",
        quantity: "12",
        percent: "11%"
    }
]);

// Calc count display circle / (1 circle = 5 product)
const circleCount = Math.ceil(listProduct.value.length / 5);

// Calc width blog all product
const widthListProduct = listProduct.value.length * 250;
// Width each blog product
const widthBlog = 250 * 5;

// Value style margin left
let marginLeft = ref(0);

// Calc when prev, next blog product
function handleArrowProduct(value) {
    marginLeft.value += value * widthBlog;

    if(marginLeft.value > 0) {
        marginLeft.value = -widthBlog * (circleCount - 1);
    } if(marginLeft.value < -widthBlog * (circleCount - 1)) {
        marginLeft.value = 0;
    }
}

// Calc when click circle
function handleCircleProduct(value) {
    marginLeft.value = -(widthBlog * value);
}

</script>