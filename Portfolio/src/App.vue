<script setup lang="ts">
import { ref } from 'vue';
import { RouterLink, RouterView } from 'vue-router'
import Copyright from "../src/components/Copyright.vue"
import { homeViewContent } from './views/home-view-content';
import Wrapper from "@/Wrapper.vue";


const isMenuShown = ref(false)

</script>

<template>
    <Wrapper>
        <header>
            <div class="router-wrapper">
                <button @click="isMenuShown = !isMenuShown" class="menuButton">
                    <div class="line" :class="{ 'whiteLine': isMenuShown }">
                    </div>
                    <div class="line" :class="{ 'whiteLine': isMenuShown }"></div>
                    <div class="line" :class="{ 'whiteLine': isMenuShown }"></div>
                </button>

                <nav>
                    <ul class="navbar">
                        <li>
                            <RouterLink to="/">Home
                            </RouterLink>
                        </li>
                        <li>
                            <RouterLink to="/work">Work</RouterLink>
                        </li>
                        <li>
                            <RouterLink to=" /about">About</RouterLink>
                        </li>
                        <li>
                            <RouterLink to="/contact">Contact
                            </RouterLink>
                        </li>
                    </ul>
                </nav>

            </div>
        </header>

        <div v-if="isMenuShown" class="openedMenu" style=" text-transform: uppercase;">
            <ul class="menu-links">
                <li>
                    <RouterLink to="/">Home
                    </RouterLink>
                </li>
                <li>
                    <RouterLink to="/work">Work</RouterLink>
                </li>
                <li>
                    <RouterLink to=" /about">About</RouterLink>
                </li>
                <li>
                    <RouterLink to="/contact">Contact</RouterLink>
                </li>
            </ul>

            <div class="menu-fullname">
                <h1 class="menu-firstName">{{ homeViewContent.firstName }}</h1>
                <h1 class="menu-astName">{{ homeViewContent.lastName }}</h1>
            </div>
        </div>

        <!-- <footer>
        <Copyright />
    </footer> -->

        <RouterView />
    </Wrapper>
</template>

<style>
html,
body {
    background-color: #D4ABB2;
    font-family: "Raleway";
}

.menuButton {
    display: flex;
    flex-direction: column;
    background-color: transparent;
    border: none;
    position: fixed;
    top: 20px;
    right: 20px;
    z-index: 1000;
}

.router-wrapper {
    font-family: "Raleway";
    text-transform: uppercase;
}

.navbar {
    display: flex;
    justify-content: flex-end;
    font-size: 25px;
    gap: 60px;
    list-style: none;
}

.navbar li a {
    text-decoration: none;
    color: #1e1e1e;
}

.openedMenu {
    display: none;
}


@media (min-width: 280px) and (max-width: 767px) {
    .navbar {
        display: none;

    }

    .line {
        width: 55px;
        height: 3px;
        background-color: black;
        margin: 3px;
    }

    .whiteLine {
        background-color: #ffff;
    }

    .openedMenu {
        display: block;
        background-color: #D4ABB2;
        color: #ffff;
        margin: 0px;
        position: fixed;
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

    .menu-links a {
        text-decoration: none;
        color: #ffff;
    }

    .menu-fullname {
        font-size: 25px;
        color: #ffff;
        text-align: right;
        margin: 12rem 4rem;
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
        gap: 50px;
    }


}

@media (min-width: 1025px) and (max-width: 1280px) {
    .navbar {
        justify-content: center;
        align-items: center;
    }
}

@media (min-width: 1900px) {
    .navbar {
        font-size: 43px;
    }
}
</style>
