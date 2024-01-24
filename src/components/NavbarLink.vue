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
            <i v-if="navLinkObj.isMore" class="bi bi-chevron-right icon"></i>
        </router-link>
    </li>
</template>

<script setup>

// Props import from components/NavbarLink.vue
const { navLinkObj } = defineProps(['navLinkObj']);
</script>