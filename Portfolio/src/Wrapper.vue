<template>
    <div :class="['main-wrapper', { dark: isDarkMode }]">
        <button @click="toggleDarkMode" class="toggle-dark-button">
            Toggle Dark Mode
        </button>
        <slot></slot>
    </div>
</template>

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

<style scoped lang="scss">
@import './assets/Variables.scss';

.main-wrapper {
    font-family: $font-family-primary;
    display: flex;
    flex-direction: column;
    background-color: $bg-color-pink-primary;
    width: 100%;

    @media (min-width: 768px) and (max-width: 1899px) {
        margin: 2rem;

    }

    @media (min-width: 1900px) {
        margin: 3rem 5rem 0 5rem;
    }
}

.main-wrapper.dark {
    background-color: #424242;
}
</style>
