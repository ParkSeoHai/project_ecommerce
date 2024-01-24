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
        icon: 'bi bi-gift',
        isMore: true
    },
    {
        id: 2,
        linkText: 'Điện thoại',
        icon: 'bi bi-phone',
        isMore: false
    },
    {
        id: 3,
        linkText: 'Apple Chính Hãng',
        icon: 'bi bi-apple',
        isMore: true
    },
    {
        id: 4,
        linkText: 'Apple Watch',
        icon: 'bi bi-smartwatch',
        isMore: true
    },
    {
        id: 5,
        linkText: 'Khuyến Mãi',
        icon: 'bi bi-gift',
        isMore: true
    },
    {
        id: 6,
        linkText: 'Điện thoại',
        icon: 'bi bi-phone',
        isMore: false
    },
    {
        id: 7,
        linkText: 'Apple Chính Hãng',
        icon: 'bi bi-apple',
        isMore: true
    },
    {
        id: 8,
        linkText: 'Apple Watch',
        icon: 'bi bi-smartwatch',
        isMore: true
    },
    {
        id: 9,
        linkText: 'Khuyến Mãi',
        icon: 'bi bi-gift',
        isMore: true
    },
    {
        id: 10,
        linkText: 'Điện thoại',
        icon: 'bi bi-phone',
        isMore: false
    },
    {
        id: 11,
        linkText: 'Apple Chính Hãng',
        icon: 'bi bi-apple',
        isMore: true
    },
    {
        id: 12,
        linkText: 'Apple Watch',
        icon: 'bi bi-smartwatch',
        isMore: true
    }
];
</script>