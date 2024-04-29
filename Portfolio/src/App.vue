<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
    <header>
        <div class="wrapper">
            <nav>
                <RouterLink to="/">Home</RouterLink>
                <RouterLink to="/work">Work</RouterLink>
                <RouterLink to="/about">About</RouterLink>
                <RouterLink to="/contact">Contact</RouterLink>

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

.wrapper {
    text-align: center;
    font-family: "coolvetica";
    text-transform: uppercase;
}

nav div {
    height: 4px;
    background-color: rgb(0, 0, 0);
    margin: 5px 0;
}

.nav {
    width: 7rem;
    margin: 3rem;
    float: right;
}
</style>
