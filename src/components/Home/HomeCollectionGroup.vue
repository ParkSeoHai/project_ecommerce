<template>
    <!-- Section product new -->
    <section class="section_collection_new">
        <div class="container p-0">
            <div class="group-collection-new">
                <div class="row">
                    <!-- Sản phẩm mới -->
                    <HomeCollectionGroupItem
                        :title="'Sản phẩm mới'"
                        :linkHref="'/sanphammoi'"
                        :listProduct="listProductNews"
                    />
                    
                    <!-- Sản phẩm bán chạy -->
                    <HomeCollectionGroupItem
                        :title="'Sản phẩm bán chạy'"
                        :linkHref="'/sanphambanchay'"
                        :listProduct="listProductHots"
                    />
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';
import HomeCollectionGroupItem from './HomeCollectionGroupItem.vue';

const listProductNews = ref([
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
        image: 'src/assets/images/applewatch-4.jpg',
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
        image: 'src/assets/images/applewatch-4.jpg',
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
    }
]);

const listProductHots = ref([
    { 
        id: 1,
        name: 'Đồng hồ thông minh XTF',
        image: 'src/assets/images/applewatch-4.jpg',
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
    }
])

</script>