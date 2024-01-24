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
                            <h2>{{ props.title }}</h2>
                            <ul class="menu-col d-flex">
                                <!-- Item link -->
                                <li><a href="#">iPhone 14 Series</a></li>
                                <li><a href="#">iPhone 14 Series</a></li>
                                <li><a href="#">iPhone 14 Series</a></li>
                                <li><a href="#">iPhone 14 Series</a></li>
                                <li><a href="#">iPhone 14 Series</a></li>
                                <li><a href="#">iPhone 14 Series</a></li>
                                <li><a href="#">iPhone 14 Series</a></li>
                            </ul>
                        </div>
                        <!-- Body -->
                        <div class="block-collection-group product-primary list-product">
                            <!-- Item -->
                            <ProductItem
                                v-for="product in props.listIphone"
                                :key="product.id"
                                :productObj="product"
                            />
                        </div>
                        <!-- Bottom -->
                        <div class="collection-bottom">
                            <div class="link">
                                <a :href="props.linkUrl">
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
const props = defineProps([
    'title',
    'linkUrl',
    'listIphone'
]);


</script>