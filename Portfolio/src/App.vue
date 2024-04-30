<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <header>
        <div class="router-wrapper">

            <div class="hamburger-menu">
                <div class="line"></div>
                <div class="line"></div>
                <div class="line"></div>

            </div>

            <nav class="navbar">
                <RouterLink style="text-decoration: none; color: #1e1e1e;" to="/">Home
                </RouterLink>
                <RouterLink style="text-decoration: none; color: #1e1e1e;" to="/work">Work</RouterLink>
                <RouterLink style="text-decoration: none; color: #1e1e1e;" to="/about">About</RouterLink>
                <RouterLink style="text-decoration: none; color: #1e1e1e;" to="/contact">Contact</RouterLink>
            </nav>

        </div>
    </header>

    <RouterView />
</template>

<style>
@font-face {
    font-family: "coolvetica";
    src: url(/Portfolio/src/fonts/coolvetica/coolvetica\ compressed\ hv.otf);
}

.router-wrapper {
    font-family: "coolvetica";
    text-transform: uppercase;
}

.navbar {
    display: flex;
    justify-content: end;
    margin: 3rem 5rem;
    font-size: 25px;
    gap: 50px;
}

@media (min-width: 280px) and (max-width: 767px) {
    .navbar {
        display: none;
    }

    .hamburger-menu {
        display: flex;
        flex-direction: column;
        align-items: end;
        margin: 30px 20px;
    }

    .line {
        width: 55px;
        height: 3px;
        background-color: black;
        margin: 3px;
    }
}

@media (min-width: 768px) and (max-width: 1024px) {
    .navbar {
        justify-content: center;
        align-items: center;
        font-size: 33px;
        gap: 50px;
    }
}

@media (min-width: 1025px) and (max-width: 1280px) {
    .navbar {
        justify-content: center;
        align-items: center;
        font-size: 35px;
        gap: 60px;
    }
}

@media (min-width: 1900px) {
    .navbar {
        font-size: 43px;
        gap: 60px;
        margin: 4rem 5rem;

    }
}
</style>
