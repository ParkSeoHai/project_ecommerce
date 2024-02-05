<template>
    <li class="item">
        <router-link 
            :to="`/`"
            class="nav-link"
            :title="`${navLinkObj.linkText}`"
        >
            <span class="content">
                <i 
                    class="icon"
                    :class="navLinkObj.icon"
                ></i>
                <span>{{ navLinkObj.linkText }}</span>
            </span>
            <i v-if="navLinkObj.subnav" class="bi bi-chevron-right icon"></i>
        </router-link>
        <!-- Sub nav -->
        <ul
            v-if="navLinkObj.subnav"
            class="nav-dropdown"
        >
            <!-- Item -->
            <li
                class="nav-dropdown__item--lv1"
                v-for="subnav in navLinkObj.subnav"
                :key="subnav.subid"
            >
                <router-link
                    :to="`/${subnav.linkUrl}`"
                    class="nav-dropdown__link lv1"
                >{{ subnav.title }}</router-link>
                <ul class="subnav-dropdown">
                    <li
                        class="nav-dropdown__item--lv2"
                        v-for="subnavItem in subnav.item"
                        :key="subnavItem.id"
                    >
                        <router-link
                            :to="`/${subnav.linkUrl}/${subnavItem.linkUrl}`"
                            class="nav-dropdown__link"
                        >{{ subnavItem.linkText }}</router-link>
                    </li>
                </ul>
            </li>
        </ul>
    </li>
</template>

<script setup>

// Props import from components/NavbarLink.vue
const { navLinkObj } = defineProps(['navLinkObj']);
</script>