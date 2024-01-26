<template>
    <div class="bg-color-white blog-group">
        <button
            v-if="props.listProduct.length > 3"
            class="btn-arrow btn-arrow-left"
            @click.prevent="handleArrowProduct(1)"
        >
            <i class="bi bi-chevron-compact-left"></i>
        </button>

        <div class="top-head d-flex justify-content-between">
            <h2>{{ props.title }}</h2>
            <a :href="props.linkHref">
                <span>Xem tất cả</span>
                <i class="bi bi-chevron-double-right"></i>
            </a>
        </div>

        <div>
            <div
                class="body-col product-new list-product"
                :style="[
                    `width: ${widthCollectionStyle}px`,
                    `grid-template-columns: repeat(${props.listProduct.length}, 1fr)`
                ]"
            >
                <ProductItem
                    v-for="product in props.listProduct"
                    :key="product.id"
                    :productObj="product"
                />
            </div>
            <ul
                class="list-circle"
            >
                <li
                    class="item"
                    
                ></li>
            </ul>
        </div>

        <button
            v-if="props.listProduct.length > 3"
            class="btn-arrow btn-arrow-right"
            @click.prevent="handleArrowProduct(1)"
        >
            <i class="bi bi-chevron-compact-right"></i>
        </button>
    </div>
</template>

<script setup>
import ProductItem from "../ProductItem.vue";

// Props import from HomeCollectionGroup.vue
const props = defineProps([
    'title', 'linkHref', 'listProduct'
]);

// Caculator width div class=`product-new list-product`
let widthCollectionStyle = props.listProduct.length * 205;

</script>