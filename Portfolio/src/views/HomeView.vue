<script setup lang="ts">
import Wrapper from "@/Wrapper.vue";
import { homeViewContent } from "./home-view-content";


</script>

<template>
    <Wrapper>
        <header class="home-wrapper">
            <div class="home-page-left-container">
                <h3 class="home-page-small-name">{{ homeViewContent.firstName }}</h3>
                <h2 class="home-page-title">{{ homeViewContent.titleCareer }}</h2>
            </div>
            <div class="home-page-right-container">
                <h2 class="home-page-firstName">{{ homeViewContent.firstName }}</h2>
                <h2 class="home-page-lastName">{{ homeViewContent.lastName }}</h2>
            </div>
        </header>
    </Wrapper>
</template>

<style src="../assets/HomeView.scss"></style>