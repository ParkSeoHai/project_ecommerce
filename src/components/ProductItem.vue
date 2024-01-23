<template>
    <div class="item">
        <div class="img">
            <a href="#">
                <img :src="props.productObj.image" :alt="props.productObj.name">
            </a>
            <!-- Hiện icon khi hover item -->
            <div class="icon-hover">
                <i class="bi bi-search"></i>
            </div>
        </div>
        <div class="content">
            <h3 class="title">
                <a :href="props.productObj.id">{{ props.productObj.name }}</a>
            </h3>
            <div>
                <ul class="list-variants pt-2">
                    <li>+{{ props.productObj.colorCount }} màu sắc</li>
                </ul>
            </div>
            <div class="box-pro-prices pt-1">
                <span>{{ props.productObj.sale }}</span>
                <del class="compare-price d-block pt-2">{{ props.productObj.price }}</del>
            </div>
            <ul class="hash-tag-loop">
                <li>Nhập tag hashtag_nội dung hiển thị để show nội dung này</li>
            </ul>
        </div>
    </div>
</template>

<script setup>
const props = defineProps(['productObj']);
</script>