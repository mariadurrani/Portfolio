<script setup lang="ts">
import { RouterLink } from 'vue-router'

</script>

<template>
    <div>
        <ul class="menu-links">
            <li>
                <RouterLink to="/" class="opened-menu-link">Home
                </RouterLink>
            </li>
            <li>
                <RouterLink to="/work" class="opened-menu-link">Work</RouterLink>
            </li>
            <li>
                <RouterLink to=" /about" class="opened-menu-link">About</RouterLink>
            </li>
            <li>
                <RouterLink to="/contact" class="opened-menu-link">Contact</RouterLink>
            </li>
        </ul>
    </div>
</template>

<style>
.menu-links {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    font-size: 60px;
    margin: 7rem;
    gap: 2rem;
    list-style: none;
    padding: 0;
}

.opened-menu-link {
    text-decoration: none;
    color: #ffff;
}
</style>