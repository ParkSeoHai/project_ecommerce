<template>
    <div class="bg-color-white">
        <div class="top-head d-flex justify-content-between">
            <h2>{{ props.title }}</h2>
            <a :href="props.linkHref">
                <span>Xem tất cả</span>
                <i class="bi bi-chevron-double-right"></i>
            </a>
        </div>
        <div style="overflow-x: scroll;">
            <div
                class="body-col d-flex product-new list-product"
                :style="{width: widthCollectionStyle + 'px'}"
            >
                <ProductItem
                    v-for="product in props.listProduct"
                    :key="product.id"
                    :productObj="product"
                />
            </div>
        </div>
    </div>
</template>

<script setup>
import ProductItem from "../ProductItem.vue";

const props = defineProps([
    'title', 'linkHref', 'listProduct'
]);

// Caculator width div class=`product-new list-product`
let widthCollectionStyle = props.listProduct.length * 210;

</script>