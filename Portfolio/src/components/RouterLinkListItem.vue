<template>
    <li>
        <RouterLink :to="props.to" :class="props.className">{{ props.text }}</RouterLink>
    </li>
</template>

<script setup lang="ts">
import { RouterLink } from 'vue-router'

interface Props {
    to: string;
    className: string;
    text: string;
}

const props = defineProps<Props>();
</script>