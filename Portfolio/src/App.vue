<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
    <header>
        <div class="router-wrapper">
            <nav class="navbar">
                <RouterLink style="text-decoration: none; color: inherit;" to="/">Home
                </RouterLink>
                <RouterLink style="text-decoration: none; color: inherit;" to="/work">Work</RouterLink>
                <RouterLink style="text-decoration: none; color: inherit;" to="/about">About</RouterLink>
                <RouterLink style="text-decoration: none; color: inherit;" to="/contact">Contact</RouterLink>
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
    margin: 4rem 10rem;
    font-size: 3rem;
    gap: 50px;
}
</style>
