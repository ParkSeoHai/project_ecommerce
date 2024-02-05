<template>
    <!-- Section Product group 1 -->
    <section class="section_collection_group">
        <div class="container p-0">
            <div class="row">
                <!-- Sản phẩm group 1 -->
                <div class="col-12">
                    <div class="bg-color-white">
                        <!-- Top -->
                        <div class="top-head d-flex justify-content-between align-items-center">
                            <h2>Điện thoại / {{ products.category.title }}</h2>
                            <ul class="menu-col d-flex">
                                <!-- Item link -->
                                <li
                                    v-for="menu in listMenu"
                                    :key="menu.subid"
                                    class="menu-item"
                                    :class="menu.subid === products.category.subid ? 'active' : ''"
                                    @click.prevent="$emit('change-product', menu)"
                                >
                                    {{ menu.title }}
                                </li>
                            </ul>
                        </div>
                        <!-- Body -->
                        <div class="block-collection-group product-primary list-product">
                            <!-- Item -->
                            <ProductItem
                                v-for="product in products.item"
                                :key="product.id"
                                :productObj="product"
                            />
                        </div>
                        <!-- Bottom -->
                        <div class="collection-bottom">
                            <div class="link">
                                <a :href="products.category.linkUrl">
                                    <span>Xem tất cả</span>
                                    <i class="bi bi-chevron-double-right"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
// Component
import ProductItem from '../ProductItem.vue';

// Props import from views/Index.vue
const { products } = defineProps(['products']);

// Menu
const listMenu = [
    {
        subid: 1,
        title: 'iPhone',
        linkUrl: 'iPhone',
    },
    {
        subid: 2,
        title: 'Samsung',
        linkUrl: 'Samsung',
    },
    {
        subid: 3,
        title: 'Oppo',
        linkUrl: 'Oppo',
    }
];

</script>