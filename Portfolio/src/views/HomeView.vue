<template>
    <Wrapper>
        <header class="home-page__wrapper">
            <div class="home-page__introduction">
                <p class="home-page__introduction__hi ">Hi! I'm</p>
                <p class="home-page__introduction__name">{{ homeViewContent.firstName + " " + homeViewContent.lastName
                    }}</p>
            </div>
            <div class="home-page__career">
                <p class="home-page__career__p">A</p>
                <p class="home-page__career__title ">{{ homeViewContent.titleCareer }}</p>
            </div>
        </header>
    </Wrapper>
</template>

<style src="../assets/HomeView.scss"></style>


<script setup lang="ts">
import Wrapper from "@/Wrapper.vue";
import { homeViewContent } from "../content/home-view-content";
</script>
