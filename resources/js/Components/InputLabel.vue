<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps({
    for: String,
    value: String,
    required: {
        type: Boolean,
        default: false,
    },
});
</script>

<template>
    <label :for="for" class="block font-medium text-sm text-gray-700">
        {{ value }}
        <span v-if="required" class="text-red-500">*</span>
    </label>
</template>
