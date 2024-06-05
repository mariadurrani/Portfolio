<template>
    <div>
        <ul class="menu-links">
            <RouterLinkListItem to="/" className="opened-menu-link" text="Home" />
            <RouterLinkListItem to="/work" className="opened-menu-link" text="Work" />
            <RouterLinkListItem to="/about" className="opened-menu-link" text="About" />
            <RouterLinkListItem to="/contact" className="opened-menu-link" text="Contact" />
        </ul>
    </div>
</template>

<style src="./RouterLinkMenu.scss"></style>

<script setup lang="ts">
import RouterLinkListItem from './RouterLinkListItem.vue';
</script>