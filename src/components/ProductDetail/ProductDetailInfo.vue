<template>
    <section class="product-detail">
        <!-- Detail -->
        <div class="row">
            <div class="col-9 product-info-detail">
                <div class="bg-color-white">
                    <div class="row">
                        <!-- Left -->
                        <div class="col-6">
                            <div class="img-active">
                                <button
                                    v-if="activeThumbnail > 0"
                                    class="btn-arrow btn-arrow-left"
                                    @click.prevent="handleImageActive(1)"
                                >
                                    <i class="bi bi-chevron-compact-left"></i>
                                </button>
                                <a href="#">
                                    <img
                                        :src="product.info[activeThumbnail].src"
                                        :alt="product.name"
                                    >
                                </a>
                                <button
                                    v-if="activeThumbnail < product.info.length - 1"
                                    class="btn-arrow btn-arrow-right"
                                    @click.prevent="handleImageActive(-1)"
                                >
                                    <i class="bi bi-chevron-compact-right"></i>
                                </button>
                            </div>
                            <div class="product-thumb">
                                <div
                                    class="list"
                                    :style="[
                                        `width: ${widthThumbnail}px`,
                                        `grid-template-columns: repeat(${product.info.length}, 1fr)`,
                                        `margin-left: ${marginLeftThumbnail}px`
                                    ]"
                                >
                                    <div
                                        v-for="(item, index) in product.info"
                                        :key="index"
                                        class="item"
                                        :class="index === activeThumbnail ? 'active' : ''"
                                        @click.prevent="activeThumbnail = index"
                                    >
                                        <img
                                            :src="item.src"
                                            :alt="product.name"
                                        >
                                    </div>
                                </div>
                            </div>
                        </div>
                        <!-- Right -->
                        <div class="col-6">
                            <div class="product-content-info">
                                <div class="title">
                                    <h1>
                                        <span class="text">{{ product.name }}</span>
                                        <span
                                            class="subtext"
                                            :class="[
                                                productQuantity > 0 ? 'green' : 'red'
                                            ]"
                                        >
                                            {{ productQuantity > 0 ? 'Còn hàng' : 'Hết hàng' }}
                                        </span>
                                    </h1>
                                </div>
                                <div class="product-info d-flex">
                                    <div class="pro-brand">
                                        <span>
                                            Thương hiệu:
                                            <a :href="product.brand.url">{{ product.brand.text }}</a>
                                        </span>
                                    </div>
                                    <span class="line-info"></span>
                                    <div class="pro-type">
                                        <span>
                                            Loại:
                                            <a :href="product.kind.url">{{ product.kind.text }}</a>
                                        </span>
                                    </div>
                                </div>
                                <div class="product-price">
                                    <span class="price-now">{{ priceSaleString }}</span>
                                    <span class="price-compare">
                                        <del>{{ priceString }}</del>
                                    </span>
                                </div>
                                <!-- Color -->
                                <div class="select-wrap">
                                    <div class="header">
                                        <div class="pro-color">
                                            <span>Màu sắc: <b class="fw-bold">{{ product.info[activeThumbnail].color }}</b></span>
                                        </div>
                                    </div>
                                    <div class="select-list py-2">
                                        <div
                                            v-for="(item, index) in product.info"
                                            :key="index"
                                            class="item"
                                            :class="[
                                                index === activeThumbnail ? 'active' : '',
                                                item.quantity > 0 ? '' : 'disabled'
                                            ]"
                                            @click.prevent="activeThumbnail = index"
                                        >
                                            <img
                                                :src="item.src"
                                                :alt="product.name">
                                            <span>{{ item.color }}</span>
                                        </div>
                                    </div>
                                </div>
                                <!-- Memory -->
                                <div class="select-wrap">
                                    <div class="header">
                                        <div class="pro-color">
                                            <span>Kích thước: <b class="fw-bold">{{ product.memory[activeMemory].total }}Gb</b></span>
                                        </div>
                                    </div>
                                    <div class="select-list py-2">
                                        <div
                                            class="item"
                                            :class="index === activeMemory ? 'active' : ''"
                                            v-for="(memory, index) in product.memory"
                                            :key="index"
                                            @click="activeMemory = index"
                                        >
                                            <span>{{ memory.total }}Gb</span>
                                        </div>
                                    </div>
                                </div>
                                <div class="selector-actions">
                                    <div class="quantity-area d-flex align-items-center justify-content-between">
                                        <button
                                            type="button"
                                            @click.prevent="count--"
                                        >-</button>
                                        <input
                                            type="text"
                                            min="1" max="999"
                                            v-model="count"
                                        >
                                        <button
                                            type="button"
                                            @click.prevent="count++"
                                        >+</button>
                                    </div>
                                </div>
                                <div class="wrap-addcart pt-3">
                                    <button
                                        class="btn btn-primary w-100"
                                        :class="productQuantity > 0 ? '' : 'disabled'"
                                        @click.prevent="addCart"
                                    >
                                        <span class="fw-bold">THÊM VÀO GIỎ</span>
                                        <span class="d-block">Giao Tận Nơi Hoặc Nhận Tại Cửa Hàng</span>
                                    </button>
                                </div>
                                <div class="location-store">
                                    <div
                                        v-if="product.locationStore.length > 0"
                                        class="location-store__main"
                                    >
                                        <img class="location-store__img" src="../../assets/images/location_store.webp" alt="">
                                        <p class="location-store__text">Có {{ product.locationStore.length }} cửa hàng còn sản phẩm</p>
                                        <button
                                            class="location-store__btn"
                                            @click.prevent="showDropdownLocationStore = !showDropdownLocationStore"
                                        >{{ showDropdownLocationStore ? '–' : '+' }}</button>
                                    </div>
                                    <div
                                        v-show="showDropdownLocationStore"
                                        class="location-store__dropdown"
                                    >
                                        <div
                                            class="item"
                                            v-for="(location, index) in product.locationStore"
                                            :key="index"
                                        >
                                            <div class="location-store__dropdown--title">
                                                <i class="bi bi-geo-alt-fill"></i>
                                                {{ location.city }}:
                                            </div>
                                            <p>{{ location.detail }}</p>
                                            <p>{{ location.description }}</p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <!-- Service -->
            <div class="col-3">
                <div class="bg-color-white">
                    <div class="service-product">
                        <div class="head-title">Cam kết bán hàng</div>
                        <ul>
                            <li>
                                <i class="bi bi-tencent-qq"></i>
                                <span class="content">Hàng chính hãng. Nguồn gốc rõ ràng</span>
                            </li>
                            <li>
                                <i class="bi bi-piggy-bank"></i>
                                <span class="content">Tặng máy nếu phát hiện máy sửa chữa</span>
                            </li>
                            <li>
                                <i class="bi bi-truck"></i>
                                <span class="content">Giao hàng ngay (nội thành TPHCM)</span>
                            </li>
                            <li>
                                <i class="bi bi-gear"></i>
                                <span class="content">Dùng thử 7 ngày miễn phí</span>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
        <!-- Description -->
        <div class="row pt-4">
            <div class="col-9">
                <ProductDescription />
            </div>
            <div class="col-3">
                <ProductSpecifications />
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref, watch, watchEffect } from "vue";
// Components
import ProductDescription from './ProductDescription.vue';
import ProductSpecifications from './ProductSpecifications.vue'

const product = {
    id: 1,
    name: 'IPhone 7 Plus - Thu Cũ IPhone 7 Plus - Thu Cũ',
    brand: {
        text: 'Apple',
        url: '/apple'
    },
    kind: {
        text: 'Apple',
        url: '/apple'
    },
    totalSale: 10,
    price: 32850000,
    info: [
        {
            quantity: 10,
            src: 'http://localhost:5173/src/assets/images/flashsale-product-3.webp',
            color: 'Đen bóng'
        },
        {
            quantity: 5,
            src: 'http://localhost:5173/src/assets/images/applewatch-4.jpg',
            color: 'Xanh'
        },
        {
            quantity: 1,
            src: 'http://localhost:5173/src/assets/images/flashsale-product-5.webp',
            color: 'Vàng'
        },
        {
            quantity: 0,
            src: 'http://localhost:5173/src/assets/images/applewatch-4.jpg',
            color: 'Đỏ'
        },
        {
            quantity: 5,
            src: 'http://localhost:5173/src/assets/images/flashsale-product-5.webp',
            color: 'Xanh than'
        },
        {
            quantity: 0,
            src: 'http://localhost:5173/src/assets/images/flashsale-product-3.webp',
            color: 'Trắng'
        }
    ],
    memory: [
        {
            total: 64,
            priceBonus: 0
        },
        {
            total: 128,
            priceBonus: 2300000
        }
    ],
    description: 'Mô tả IPhone 7 Plus - Thu Cũ IPhone 7 Plus - Thu Cũ',
    locationStore: [
        {
            city: 'Hồ Chí Minh',
            detail: '59A âu cơ, Phường 14, Quận 11',
            description: 'Mở cửa: 9 giờ 00 - 22 giờ (Các ngày trong tuần)'
        },
        {
            city: 'Hà Nội',
            detail: 'Nguyễn Cơ Thạch, Mỹ Đình, Nam Từ Liêm',
            description: 'Mở cửa: 9 giờ 00 - 22 giờ (Các ngày trong tuần)'
        }
    ]
};

// Calc width block thumbnail - 1 item: 95px
const widthThumbnail = product.info.length * 95;

// Variable storage value active thumbnail
let activeThumbnail = ref(0);
// Variable storage value active memory
let activeMemory = ref(0);

// Count add to cart
let count = ref(1);

// Price product
let price = ref(product.price);
// Price sale
let priceSale = ref(price.value - (product.totalSale / 100) * product.price);

// Format price to vnd
const formatterPrice = new Intl.NumberFormat("vi-VN", {
  style: "currency",
  currency: "VND",
});

// Price display
let priceString = formatterPrice.format(price.value);
// Price sale display
let priceSaleString = formatterPrice.format(priceSale.value);

// Calc quantity product
let productQuantity = 0;
product.info.map((item) => {
    productQuantity += item.quantity;
});

// Variable value margin-left style
let marginLeftThumbnail = ref(0);

// Is show dropdown location store
let showDropdownLocationStore = ref(false);

// Handle click button next/prev image active
function handleImageActive(n) {
    activeThumbnail.value -= n;
}

// Handle add product to cart
function addCart() {
    const cartItem = {
        name: product.name,
        imageSrc: product.info[activeThumbnail.value],
        memory: product.memory[activeMemory.value],
        price: priceSale.value,
        quantity: count.value
    }

    console.log(cartItem);
}

// Watch activeThumbnail -> Calc value margin-left
watchEffect(() => {
    // Handle style value margin-left thumbnail
    if(product.info.length < 5) {
        marginLeftThumbnail.value = 0;
    } else if(activeThumbnail.value + 5 >= product.info.length) {
        marginLeftThumbnail.value = -(product.info.length - 5) * 95;
    } else {
        marginLeftThumbnail.value = -(activeThumbnail.value * 95);
    }

    if(product.info.length - activeThumbnail.value >= 5 && activeThumbnail.value > 0) {
        marginLeftThumbnail.value += 95;
    }
})

// Watch activeMemory -> Calc value price product
watch(activeMemory, () => {
    // Handle calculator price
    let priceBonus = product.memory[activeMemory.value].priceBonus;
    if(priceBonus === 0) {
        price.value = product.price;
    } else {
        price.value += priceBonus;
    }
    // Calc price sale
    priceSale.value = price.value - (product.totalSale / 100) * price.value;

    // Update price and price sale string display
    priceString = formatterPrice.format(price.value)
    priceSaleString = formatterPrice.format(priceSale.value);
})

// Watch handle count add cart
watch(count, () => {
    // If it not a number
    if(isNaN(count.value)) {
        count.value = 1;
    } else if(count.value < 1) {
        count.value = 1;
    } else if(count.value > product.quantity) {
        count.value = product.quantity;
    }
})

</script>