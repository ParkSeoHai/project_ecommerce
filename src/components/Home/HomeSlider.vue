<template>
    <!-- Home Slider -->
    <section id="home-slider" class="home-slider">
        <div class="container p-0">
            <div class="row">
                <div class="col-3">
                    <!-- Navbar -->
                    <Navbar />
                </div>
                <div class="col-9 pt-3 ps-0 home-banner-slider">
                    <div 
                        class="banner-slider"
                    >
                        <button
                            v-if="imageSliders.length > 1"
                            @click.prevent="showSlider(-1)"
                            class="btn-arrow btn-arrow-left"
                        >
                            <i class="bi bi-chevron-compact-left"></i>
                        </button>
                        <a 
                            :href="sliderShow.link" 
                            class="slider-link"
                        >
                            <img
                                :src="sliderShow.image"
                                alt=""
                            >
                        </a>
                        <button
                            v-if="imageSliders.length > 1"
                            @click.prevent="showSlider(1)"
                            class="btn-arrow btn-arrow-right"
                        >
                            <i class="bi bi-chevron-compact-right"></i>
                        </button>
                        <ul
                            class="list-circle"
                            v-if="imageSliders.length > 1"
                        >
                            <li 
                                class="item"
                                v-for="n in imageSliders.length"
                                :key="n"
                                :class="sliderIndex === n - 1 ? 'active' : ''"
                                @click.prevent="handleCircle(n - 1)"
                            ></li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref, watch } from 'vue';
import Navbar from '../Navbar.vue';

// Slider show
const imageSliders = [
    {
        image: 'src/assets/images/banner-slider-1.webp',
        link: '/slider-1'
    },
    {
        image: 'src/assets/images/banner-slider-2.webp',
        link: '/slider-2'
    },
    {
        image: 'src/assets/images/banner-slider-3.webp',
        link: '/slider-3'
    }
];

// Slider index showing
let sliderIndex = ref(0);
// Slider is showing
let sliderShow = ref(imageSliders[sliderIndex.value]);

watch(
    sliderIndex,
    () => {
        sliderShow.value = imageSliders[sliderIndex.value];
    }
)

// Next slider after 10s
setInterval(() => {
    showSlider(1);
}, 10000);

// Calc value slider index active
function showSlider(n) {
    sliderIndex.value += n;
    if(sliderIndex.value > imageSliders.length - 1) {
        sliderIndex.value = 0;
    }
    if(sliderIndex.value < 0) {
        sliderIndex.value = imageSliders.length - 1;
    }
}

// Handle when click circle item
function handleCircle(n) {
    sliderIndex.value = n;
}

</script>