<script setup lang="ts">
import Wrapper from "@/Wrapper.vue";
import Copyright from "../components/Copyright.vue"
import { homeViewContent } from "./home-view-content";


</script>

<template>
    <Wrapper>

        <!-- default layout -->
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
        <!-- default layout -->
    </Wrapper>

</template>

<style>
.home-wrapper {
    font-family: 'Raleway';
    text-transform: uppercase;
    letter-spacing: -2px;

}

.home-page-left-container {
    display: flex;
    flex-direction: column;
    color: #1e1e1e;
    font-size: 20px;
    margin-top: 5rem;

}

.home-page-small-name,
.home-page-title {
    margin: 0;
}

.home-page-title {
    font-size: 100px;
    width: 15rem;
}

.home-page-right-container {
    display: flex;
    flex-direction: column;
    font-size: 50px;
    color: #1e1e1e;
    align-self: flex-end;
    text-align: right;
    margin-top: 5rem;

}

.home-page-firstName,
.home-page-lastName {
    margin: 0;
}

@media (min-width: 280px) and (max-width: 767px) {
    .home-page-left-container {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .home-page-title {
        font-size: 40px;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    .home-page-rightcontainer {
        font-size: 20px;
        justify-content: center;
        align-items: center;
    }

    .home-page-small-name {
        font-size: 20px;
    }
}

@media (min-width: 768px) and (max-width: 1024px) {
    .home-wrapper {
        padding: 10px;
    }

    .home-page-title {
        font-size: 60px;
    }

    .home-page-right-container {
        font-size: 32px;
    }
}

@media (min-width: 1025px) and (max-width: 1280px) {

    .home-page-title {
        font-size: 65px;
        width: 20rem;
    }

    .home-page-right-container {
        font-size: 33px;
    }
}

@media (min-width: 1281px) and (max-width: 1899px) {

    .home-page-left-container {
        margin-top: 5rem;
    }

    .home-page-title {
        font-size: 75px;
        width: 20rem;
    }

    .home-page-right-container {
        font-size: 40px;
    }
}

@media (min-width: 1900px) {
    .home-page-right-container {
        margin-top: 15rem;
    }

}
</style>