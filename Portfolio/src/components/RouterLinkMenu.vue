<script setup lang="ts">
import RouterLinkListItem from './RouterLinkListItem.vue';
</script>

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