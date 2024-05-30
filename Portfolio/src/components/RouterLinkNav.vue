<script setup lang="ts">
import { RouterLink } from 'vue-router'

</script>

<template>
    <div>
        <ul class="navbar">
            <!-- Todo: We need to add a RouterLinkListItem component and pass props dynamically to it. -->
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

<style src="../assets/RouterLinkListItemNav.scss"></style>
