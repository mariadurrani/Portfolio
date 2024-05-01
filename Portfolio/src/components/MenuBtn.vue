<script setup lang="ts">

defineEmits(['userClicked'])

</script>

<template>
    <div @click="$emit('userClicked')">click me
    </div>
</template>