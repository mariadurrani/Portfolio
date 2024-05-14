<script setup lang="ts">
import Wrapper from "@/Wrapper.vue";
import Copyright from "../components/Copyright.vue"
import { homeViewContent } from "./home-view-content";


</script>

<template>
    <Wrapper>
        <header class="home-wrapper">
            <div class="home-page-left-container">
                <h2 class="home-page-small-name">{{ homeViewContent.firstName }}</h2>
                <h1 class="home-page-title">{{ homeViewContent.titleCareer }}</h1>
            </div>
            <div class="home-page-right-container">
                <h1 class="home-page-firstName">{{ homeViewContent.firstName }}</h1>
                <h1 class="home-page-lastName">{{ homeViewContent.lastName }}</h1>
            </div>
        </header>
    </Wrapper>

</template>

<style src="../assets/HomeView.css"></style>