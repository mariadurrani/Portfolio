<template>
    <Wrapper>
        <header>
            <div class="router-wrapper">
                <div class="mobile__navigation" id="navBar">
                    <span class="mobile__menu-button" @click="openNav">&#9776;</span>
                    <RouterLinkNav />
                </div>
            </div>
        </header>

        <nav id="mobileNav" class="overlay">
            <a href="javascript:void(0)" class="closebtn" @click="closeNav">&times;</a>
            <RouterLinkMenu />
        </nav>
        <RouterView />
    </Wrapper>
</template>

<style src="./assets/App.scss"></style>

<script setup lang="ts">
import { RouterView } from 'vue-router'
import RouterLinkNav from './components/RouterLinkNav.vue';
import RouterLinkMenu from './components/RouterLinkMenu.vue';
import Wrapper from './components/Wrapper.vue';

function openNav() {
    document.getElementById("mobileNav")!.style.width = "90%";
}

function closeNav() {
    document.getElementById("mobileNav")!.style.width = "0%";
}

const body = document.body;
let lastScroll = 0;

window.addEventListener

</script>
