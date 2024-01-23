<template>
    <li class="item">
        <router-link 
            :to="`/`"
            class="nav-link"
            :title="`${props.linkText}`"
        >
            <span class="content">
                <i 
                    class="icon"
                    :class="props.icon"
                ></i>
                <span>{{ props.linkText }}</span>
            </span>
            <i v-if="isMore" class="bi bi-chevron-right icon"></i>
        </router-link>
    </li>
</template>

<script setup>
const props = defineProps(['linkText', 'icon', 'isMore']);
</script>