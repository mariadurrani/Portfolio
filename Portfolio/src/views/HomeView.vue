<script setup lang="ts">
import Copyright from "../components/Copyright.vue"
import { homeViewContent } from "./home-view-content";



</script>

<template>
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
</template>

<style>
.home-wrapper {
    font-family: "Raleway";
    text-transform: uppercase;
}


.homepage-leftcontainer {
    display: flex;
    flex-direction: column;
    color: #1e1e1e;
    font-size: 20px;
}

.home-smallName,
.homepage-title {
    margin: 0;
}

.homepage-title {
    font-size: 100px;
    width: 15rem;
    letter-spacing: -2px;

}

.homepage-rightcontainer {
    display: flex;
    flex-direction: column;
    font-size: 50px;
    color: #1e1e1e;
    letter-spacing: -2px;
    align-self: flex-end;
    text-align: right;
}

.home-firstName,
.home-lastName {
    margin: 0;
}


@media (min-width: 280px) and (max-width: 767px) {
    .homepage-leftcontainer {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        margin-top: 8rem;
    }

    .homepage-title {
        font-size: 49px;
    }

    .homepage-rightcontainer {
        font-size: 25px;
        justify-content: center;
        margin-top: 5rem;
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
    .homepage-leftcontainer {
        margin: 7rem 6rem;
    }

    .homepage-title {
        font-size: 65px;
        width: 20rem;
    }

    .homepage-rightcontainer {
        font-size: 33px;
        margin: 25rem 6rem 0 0;
    }
}

@media (min-width: 1281px) and (max-width: 1899px) {
    .homepage-leftcontainer {
        margin: 7rem 6rem;
    }

    .homepage-title {
        font-size: 75px;
        width: 20rem;
    }

    .homepage-rightcontainer {
        font-size: 40px;
        margin: 26rem 6rem 0 0;
    }
}
</style>