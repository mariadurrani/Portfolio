<script setup lang="ts">
import { ref } from 'vue';
import { RouterLink, RouterView } from 'vue-router'
import Copyright from "../src/components/Copyright.vue"
import { homeViewContent } from './views/home-view-content';

const isMenuShown = ref(false)


</script>

<template>
    <header>
        <div class="router-wrapper">
            <button @click="isMenuShown = !isMenuShown" class="menuButton">
                <div class="line"></div>
                <div class="line"></div>
                <div class="line"></div>
            </button>

            <nav>
                <ul class="navbar">
                    <li>
                        <RouterLink style="text-decoration: none; color: #1e1e1e; ;" to="/">Home
                        </RouterLink>
                    </li>
                    <li>
                        <RouterLink style="text-decoration: none; color: #1e1e1e; " to="/work">Work</RouterLink>
                    </li>
                    <li>
                        <RouterLink style="text-decoration: none; color: #1e1e1e;" to="/about">About</RouterLink>
                    </li>
                    <li>
                        <RouterLink style="text-decoration: none; color: #1e1e1e;" to="/contact">Contact</RouterLink>
                    </li>
                </ul>
            </nav>

        </div>
    </header>

    <div v-if="isMenuShown" class="openedMenu" style="font-family: 'RalewayBold'; text-transform: uppercase;">
        <ul class="menu-links">
            <li>
                <RouterLink style="text-decoration: none; color: #ffff; ;" to="/">Home
                </RouterLink>
            </li>
            <li>
                <RouterLink style="text-decoration: none; color: #ffff; " to="/work">Work</RouterLink>
            </li>
            <li>
                <RouterLink style="text-decoration: none; color: #ffff;" to="/about">About</RouterLink>
            </li>
            <li>
                <RouterLink style="text-decoration: none; color: #ffff;" to="/contact">Contact</RouterLink>
            </li>
        </ul>

        <div class="menu-fullName">
            <h1 class="menu-firstName">{{ homeViewContent.firstName }}</h1>
            <h1 class="menu-lastName">{{ homeViewContent.lastName }}</h1>
        </div>



    </div>

    <RouterView />
</template>

<style>
html,
body {
    background-color: #D4ABB2;
    font-family: "Raleway";
    text-transform: uppercase;
}

.menuButton {
    display: flex;
    flex-direction: column;
    background-color: transparent;
    border: none;
    z-index: 1000;
    margin: 1rem 20rem;
}

.line {
    width: 55px;
    height: 3px;
    background-color: black;
    margin: 3px;
}


.router-wrapper {
    font-family: "Raleway";
    text-transform: uppercase;
}

.navbar {
    display: flex;
    justify-content: flex-end;
    margin: 4rem 5rem;
    font-size: 43px;
    gap: 60px;
    list-style: none;
}

@media (min-width: 280px) and (max-width: 767px) {
    .navbar {
        display: none;
    }

    .openedMenu {

        background-color: #D4ABB2;
        color: #ffff;
        position: fixed;
        margin: 40px;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
    }

    .menu-links {
        display: flex;
        flex-direction: column;
        font-size: 60px;
    }

    .menu-links li {
        margin-top: 20px;
        padding: 8px;
        list-style: none;
    }

    .menu-fullName {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        font-size: 22px;
        color: #ffffffa4;
        margin: 3rem 2rem;
    }

    .menu-firstName,
    .menu-lastName {
        margin: 0;
    }

}


@media (min-width: 768px) and (max-width: 1024px) {
    .navbar {
        justify-content: center;
        align-items: center;
        font-size: 28px;
        gap: 50px;
    }
}

@media (min-width: 1025px) and (max-width: 1280px) {
    .navbar {
        justify-content: center;
        align-items: center;
        font-size: 30px;
    }
}

@media (min-width: 1281px) and (max-width: 1899px) {
    .navbar {
        font-size: 35px;
    }
}
</style>
