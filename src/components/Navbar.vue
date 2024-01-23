<template>
    <nav class="nav-group">
        <ul class="list-menu-nav">
            <NavbarLink
                :linkText="'Khuyễn Mãi'"
                :icon="'bi bi-gift'"
                :isMore="true"
            />
            <NavbarLink
                :linkText="'Điện thoại'"
                :icon="'bi bi-phone'"
            />
            <NavbarLink
                :linkText="'Apple Chính hãng'"
                :icon="'bi bi-apple'"
            />
            <NavbarLink
                :linkText="'Apple Watch'"
                :icon="'bi bi-smartwatch'"
            />

            <NavbarLink
                :linkText="'Khuyễn Mãi'"
                :icon="'bi bi-gift'"
            />
            <NavbarLink
                :linkText="'Điện thoại'"
                :icon="'bi bi-phone'"
            />
            <NavbarLink
                :linkText="'Apple Chính hãng'"
                :icon="'bi bi-apple'"
            />
            <NavbarLink
                :linkText="'Apple Watch'"
                :icon="'bi bi-smartwatch'"
            />
            <NavbarLink
                :linkText="'Khuyễn Mãi'"
                :icon="'bi bi-gift'"
            />
            <NavbarLink
                :linkText="'Điện thoại'"
                :icon="'bi bi-phone'"
            />
            <NavbarLink
                :linkText="'Apple Chính hãng'"
                :icon="'bi bi-apple'"
            />
            <NavbarLink
                :linkText="'Apple Watch'"
                :icon="'bi bi-smartwatch'"
            />

            <!-- <li class="item">
                <a href="" class="nav-link">
                    <span class="content">
                        <i class="bi bi-phone icon"></i>
                        <span>Điện thoại</span>
                    </span>
                    <i class="bi bi-chevron-right icon"></i>
                </a>
            </li> -->
        </ul>
    </nav>
</template>

<script setup>
import NavbarLink from './NavbarLink.vue';
</script>