<script setup lang="ts">
import { RouterLink } from 'vue-router'

</script>

<template>
    <div>
        <ul class="navbar">
            <li>
                <RouterLink to="/" class="navbar-link">Home
                </RouterLink>
            </li>
            <li>
                <RouterLink to="/work" class="navbar-link">Work</RouterLink>
            </li>
            <li>
                <RouterLink to=" /about" class="navbar-link">About</RouterLink>
            </li>
            <li>
                <RouterLink to="/contact" class="navbar-link">Contact
                </RouterLink>
            </li>
        </ul>
    </div>
</template>

<style>
.navbar {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 25px;
    gap: 60px;
    list-style: none;
}

.navbar-link {
    text-decoration: none;
    color: #1e1e1e;
}

@media (max-width: 767px) {
    .navbar {
        display: none;
    }
}

@media (min-width: 1025px) and (max-width: 1200px) {

    .navbar {
        gap: 80px;
    }
}

@media (min-width: 1201px) and (max-width: 1899px) {
    .navbar {
        display: flex;
        justify-content: flex-end;
        gap: 80px;
    }
}

@media (min-width: 1900px) {
    .navbar {
        font-size: 35px;
        display: flex;
        justify-content: flex-end;
        gap: 80px;
    }
}
</style>
