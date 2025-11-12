<script setup>
defineProps({
    bg: {
        type: String,
        default: 'bg-gray-100'
    }
})
</script>

<template>
    <div :class="`${bg} p-10 rounded-lg shadow-md`">
        <slot></slot>
    </div>
</template>