<template>
    <div :class="['main-wrapper', { dark: isDarkMode }]">
        <div @click="toggleDarkMode" class="toggle-dark-button">
        </div>
        <slot></slot>
    </div>
</template>

<style src="../src/assets/Wrapper.scss">
@import './assets/Variables.scss';
</style>

<script>
export default {
    data() {
        return {
            isDarkMode: false
        };
    },
    methods: {
        toggleDarkMode() {
            this.isDarkMode = !this.isDarkMode;
        }
    }
};

</script>
