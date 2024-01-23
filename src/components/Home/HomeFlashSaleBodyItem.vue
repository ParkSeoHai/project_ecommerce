<template>
    <div class="item">
        <div class="img">
            <a href="#">
                <img :src="props.imageUrl" :alt="props.productName">
            </a>
            <!-- Hiện icon khi hover item -->
            <div class="icon-hover">
                <i class="bi bi-search"></i>
            </div>
        </div>
        <div class="content">
            <h3 class="title">
                <a href="#">{{ props.productName }}</a>
            </h3>
            <div>
                <ul class="list-variants pt-2">
                    <li>+{{ props.colorCount }} màu sắc</li>
                </ul>
            </div>
            <div class="box-pro-prices pt-1 d-flex align-items-center">
                <span>{{ props.productSale }}</span>
                <del class="compare-price ps-3">{{ props.productPrice }}</del>
            </div>
            <ul class="hash-tag-loop">
                <li>Nhập tag hashtag_nội dung hiển thị để show nội dung này</li>
            </ul>
            <div class="fl_progressbar_group d-flex align-items-center">
                <div class="icon d-flex align-items-center">
                    <i class="bi bi-fire"></i>
                </div>
                <span v-if="props.quantity >= 90">Sắp cháy hàng</span>
                <span v-else>Đã bán <strong>{{ props.quantity }}</strong> sản phẩm</span>
            </div>

            <div class="fl_progressbar">
                <div class="fl_percent" :style="{width: props.percent}"></div>
            </div>
       </div>
   </div>
</template>

<script setup>
const props = defineProps([
   'imageUrl', 'productName', 'colorCount', 'productPrice', 'productSale', 'quantity', 'percent'
]);
</script>