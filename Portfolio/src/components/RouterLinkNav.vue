<template>

    <div>
        <ul class="navbar">
            <RouterLinkListItem to="/" className="navbar-link" text="Home" />
            <RouterLinkListItem to="/work" className="navbar-link" text="Work" />
            <RouterLinkListItem to="/about" className="navbar-link" text="About" />
            <RouterLinkListItem to="/contact" className="navbar-link" text="Contact" />
        </ul>
    </div>
</template>

<style src="./RouterLinkNav.scss"></style>

<script setup lang="ts">
import RouterLinkListItem from './RouterLinkListItem.vue';
</script>
