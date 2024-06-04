<template>
    <Wrapper>
        <header class="home-page__wrapper">
            <div class="home-page__career-container">
                <p class="home-page__career-container__first-name">{{ homeViewContent.firstName }}</p>
                <h1 class="home-page__career-container__title">{{ homeViewContent.titleCareer }}</h1>
            </div>
            <div class="home-page__fullname-container">
                <h2 class="home-page__fullname-container__firstName">{{ homeViewContent.firstName }}</h2>
                <h2 class="home-page__fullname-container__lastName">{{ homeViewContent.lastName }}</h2>
            </div>
        </header>
    </Wrapper>
</template>

<style src="../assets/HomeView.scss"></style>


<script setup lang="ts">
import Wrapper from "@/Wrapper.vue";
import { homeViewContent } from "../content/home-view-content";
</script>
