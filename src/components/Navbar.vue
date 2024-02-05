<template>
    <nav class="nav-group">
        <ul class="list-menu-nav">
            <NavbarLink
                v-for="navLink in listNavLinks"
                :key="navLink.id"
                :navLinkObj="navLink"
            />
        </ul>
    </nav>
</template>

<script setup>
import NavbarLink from './NavbarLink.vue';

const listNavLinks = [
    {
        id: 1,
        linkText: 'Khuyến Mãi',
        linkUrl: 'khuyen-mai',
        icon: 'bi bi-gift',
    },
    {
        id: 2,
        linkText: 'Điện thoại',
        linkUrl: 'dien-thoai',
        icon: 'bi bi-phone',
        subnav: [
            {
                subid: 1,
                title: 'iPhone',
                linkUrl: 'iPhone',
                item: [
                    {
                        id: 1,
                        linkText: 'iPhone 14 Series',
                        linkUrl: 'iPhone-14-Series'
                    },
                    {
                        id: 2,
                        linkText: 'iPhone 13 Series',
                        linkUrl: 'iPhone-13-Series'
                    },
                    {
                        id: 3,
                        linkText: 'iPhone 12 Series',
                        linkUrl: 'iPhone-12-Series'
                    },
                    {
                        id: 4,
                        linkText: 'iPhone 11 Series',
                        linkUrl: 'iPhone-11-Series'
                    },
                    {
                        id: 5,
                        linkText: 'iPhone 15 Series',
                        linkUrl: 'iPhone-15-Series'
                    }
                ]
            },
            {
                subid: 1,
                title: 'Samsung',
                linkUrl: 'samsung',
                item: [
                    {
                        id: 1,
                        linkText: 'S23 Series',
                        linkUrl: 's23-series'
                    },
                    {
                        id: 2,
                        linkText: 'S24 Series',
                        linkUrl: 's24-series'
                    }
                ]
            }
        ]
    },
    {
        id: 3,
        linkText: 'Apple Chính Hãng',
        icon: 'bi bi-apple',
    },
    {
        id: 4,
        linkText: 'Apple Watch',
        icon: 'bi bi-smartwatch',
    },
    {
        id: 5,
        linkText: 'Khuyến Mãi',
        icon: 'bi bi-gift',
    },
    {
        id: 6,
        linkText: 'Điện thoại',
        icon: 'bi bi-phone',
    },
    {
        id: 7,
        linkText: 'Apple Chính Hãng',
        icon: 'bi bi-apple',
    },
    {
        id: 8,
        linkText: 'Apple Watch',
        icon: 'bi bi-smartwatch',
    },
    {
        id: 9,
        linkText: 'Khuyến Mãi',
        icon: 'bi bi-gift',
    },
    {
        id: 10,
        linkText: 'Điện thoại',
        icon: 'bi bi-phone',
    },
    {
        id: 11,
        linkText: 'Apple Chính Hãng',
        icon: 'bi bi-apple',
    },
    {
        id: 12,
        linkText: 'Apple Watch',
        icon: 'bi bi-smartwatch',
    }
];
</script>