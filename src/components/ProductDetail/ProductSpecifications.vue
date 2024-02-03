<template>
    <div class="bg-color-white">
        <div class="product-desc-tab">
            <div class="product-desc-tab__title">
                Thông số kĩ thuật
            </div>
            
            <div
                class="product-desc-tab__content"
                :class="showViewAll ? 'show' : ''"
            >
                <p>Thông số kĩ thuật</p>
            </div>

            <div class="view-all-tab">
                <button
                    class="view-all-tab__btn"
                    @click.prevent="showViewAll = !showViewAll"
                >
                    <i
                        class="bi view-all-tab__btn--icon"
                        :class="showViewAll ? 'bi-dash-circle' : 'bi-plus-circle'"
                    ></i>
                    {{ showViewAll ? 'Rút gọn' : 'Xem thêm' }}
                </button>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from "vue";

let showViewAll = ref(false);
</script>