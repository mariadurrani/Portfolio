<script setup lang="ts">
import Wrapper from "@/Wrapper.vue";
import Copyright from "../components/Copyright.vue"
import { homeViewContent } from "./home-view-content";


</script>

<template>
    <Wrapper>

        <!-- default layout -->
        <header class="home-wrapper">
            <div class="homepage-leftcontainer">
                <h2 class="home-smallName">{{ homeViewContent.firstName }}</h2>
                <h1 class="homepage-title">{{ homeViewContent.titleCareer }}</h1>
            </div>
            <div class="homepage-rightcontainer">
                <h1 class="home-firstName">{{ homeViewContent.firstName }}</h1>
                <h1 class="home-lastName">{{ homeViewContent.lastName }}</h1>
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

.homepage-leftcontainer {
    display: flex;
    flex-direction: column;
    color: #1e1e1e;
    font-size: 20px;
    margin-top: 5rem;

}

.home-smallName,
.homepage-title {
    margin: 0;
}

.homepage-title {
    font-size: 100px;
    width: 15rem;
}

.homepage-rightcontainer {
    display: flex;
    flex-direction: column;
    font-size: 50px;
    color: #1e1e1e;
    align-self: flex-end;
    text-align: right;
    margin-top: 5rem;

}

.home-firstName,
.home-lastName {
    margin: 0;
}

@media (min-width: 280px) and (max-width: 767px) {
    .homepage-leftcontainer {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .homepage-title {
        font-size: 40px;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    .homepage-rightcontainer {
        font-size: 20px;
        justify-content: center;
        align-items: center;
    }

    .home-smallName {
        font-size: 20px;
    }
}

@media (min-width: 768px) and (max-width: 1024px) {
    .home-wrapper {
        padding: 10px;
    }

    .homepage-title {
        font-size: 60px;
    }

    .homepage-rightcontainer {
        font-size: 32px;
    }
}

@media (min-width: 1025px) and (max-width: 1280px) {

    .homepage-title {
        font-size: 65px;
        width: 20rem;
    }

    .homepage-rightcontainer {
        font-size: 33px;
    }
}

@media (min-width: 1281px) and (max-width: 1899px) {

    .homepage-leftcontainer {
        margin-top: 5rem;
    }

    .homepage-title {
        font-size: 75px;
        width: 20rem;
    }

    .homepage-rightcontainer {
        font-size: 40px;
    }
}

@media (min-width: 1900px) {
    .homepage-rightcontainer {
        margin-top: 15rem;
    }

}
</style>