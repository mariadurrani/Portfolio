<script setup lang="ts">
</script>

<template>
    <div class="main-wrapper">

        <slot></slot>
    </div>
</template>

<style scoped>
.main-wrapper {
    font-family: "Raleway";
    display: flex;
    flex-direction: column;

    @media (min-width: 768px) and (max-width: 1899px) {
        margin: 3rem;
    }

    @media (min-width: 1900px) {
        margin: 3rem 5rem 0 5rem;
    }
}
</style>