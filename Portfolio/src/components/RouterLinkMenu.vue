<script setup lang="ts">
import { RouterLink } from 'vue-router'

</script>

<template>
    <div>
        <ul class="menu-links">
            <!-- Todo: We need to add a RouterLinkListItem component and pass props dynamically to it. -->
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

<style src="../assets/RouterLinkListItemMenu.scss"></style>