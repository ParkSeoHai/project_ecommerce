<template>
    <section id="section-category">
        <div class="container p-0">
            <div class="bg-color-white">
                <div class="list-cat d-flex justify-content-between">
                    <!-- Item -->
                    <HomeCategoryItem 
                        :imageUrl="'src/assets/images/applewatch-2.jpg'"
                        :categoryName="'Apple Watch DZ09'"
                    />
                    <!-- Item -->
                    <HomeCategoryItem 
                        :imageUrl="'src/assets/images/section-category-2.png'"
                        :categoryName="'Samsung S23 Series'"
                    />
                    <!-- Item -->
                    <HomeCategoryItem 
                        :imageUrl="'src/assets/images/section-category-3.png'"
                        :categoryName="'Samsung S23 Series'"
                    />
                    <!-- Item -->
                    <HomeCategoryItem 
                        :imageUrl="'src/assets/images/section-category-4.png'"
                        :categoryName="'Xiaomi Redmi Note 12'"
                    />
                    <!-- Item -->
                    <HomeCategoryItem 
                        :imageUrl="'src/assets/images/applewatch-2.jpg'"
                        :categoryName="'Apple Watch DZ09'"
                    />
                    <!-- Item -->
                    <HomeCategoryItem 
                        :imageUrl="'src/assets/images/section-category-2.png'"
                        :categoryName="'Samsung S23 Series'"
                    />
                    <!-- Item -->
                    <HomeCategoryItem 
                        :imageUrl="'src/assets/images/section-category-3.png'"
                        :categoryName="'Samsung S23 Series'"
                    />
                    <!-- Item -->
                    <HomeCategoryItem 
                        :imageUrl="'src/assets/images/section-category-4.png'"
                        :categoryName="'Xiaomi Redmi Note 12'"
                    />
                    <!-- Item -->
                    <HomeCategoryItem 
                        :imageUrl="'src/assets/images/section-category-3.png'"
                        :categoryName="'Samsung S23 Series'"
                    />
                    <!-- Item -->
                    <HomeCategoryItem 
                        :imageUrl="'src/assets/images/section-category-4.png'"
                        :categoryName="'Xiaomi Redmi Note 12'"
                    />
                    <!-- Item -->
                    <HomeCategoryItem 
                        :imageUrl="'src/assets/images/section-category-4.png'"
                        :categoryName="'Xiaomi Redmi Note 12'"
                    />
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import HomeCategoryItem from './HomeCategoryItem.vue';
</script>