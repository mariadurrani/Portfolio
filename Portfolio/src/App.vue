<script setup lang="ts">
import { ref } from 'vue';
import { RouterView } from 'vue-router'
import { homeViewContent } from './views/home-view-content';
import Wrapper from "@/Wrapper.vue";
import RouterLinkNav from './components/RouterLinkNav.vue';
import RouterLinkMenu from './components/RouterLinkMenu.vue';

const isMenuShown = ref(false)

</script>

<template>
    <Wrapper>
        <header>
            <div class="router-wrapper">
                <button @click="isMenuShown = !isMenuShown" class="menu-button-container">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512" class="menu-button">
                        <path v-if="!isMenuShown"
                            d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z" />
                        <path v-else="isMenuShown" fill="#ffffff"
                            d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z" />
                    </svg>
                </button>

                <nav>
                    <RouterLinkNav />
                </nav>
            </div>
        </header>

        <div v-if="isMenuShown" class="opened-menu">
            <RouterLinkMenu />
            <div class="menu-fullname">
                <h1 class="menu-firstName">{{ homeViewContent.firstName }}</h1>
                <h1 class="menu-lastName">{{ homeViewContent.lastName }}</h1>
            </div>
        </div>
        <RouterView />
    </Wrapper>
</template>

<style src="./assets/App.css"></style>
