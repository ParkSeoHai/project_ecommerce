<template>
    <!-- Header -->
    <header class="header">
        <!-- Header top -->
        <HeaderTop @handle-modal="handleModal" />
        <!-- Header bottom -->
        <HeaderBottom />
    </header>
</template>

<script setup>
// Component
import HeaderTop from './HeaderTop.vue';
import HeaderBottom from './HeaderBottom.vue';

const $emits = defineEmits(['handle-modal']);

// Handle emit event to App.vue
function handleModal(value) {
    $emits('handle-modal', value);
}
</script>