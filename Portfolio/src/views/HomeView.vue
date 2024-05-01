<script setup lang="ts">
import Copyright from "../components/Copyright.vue"

const firstName = "Maria"
const lastName = "Durrani"
const titleCareer = "Frontend Developer"

</script>

<template>
    <header class="home-wrapper">
        <main>
            <div class="left-container">
                <h2 class="leftName">{{ firstName }}</h2>
                <h1 class="leftTitleCareer">{{ titleCareer }}</h1>
            </div>
            <div class="right-container">
                <h1 class="rightFirstName">{{ firstName }}</h1>
                <h1 class="rightLastName">{{ lastName }}</h1>
            </div>
        </main>
    </header>
    <footer>
        <Copyright />
    </footer>

</template>

<style>
.home-wrapper {
    font-family: "coolvetica";
    text-transform: uppercase;
}

.left-container {
    display: flex;
    flex-direction: column;
    margin: 4rem 10rem;
    color: #1e1e1e;
    font-size: 20px;
}

.leftName,
.leftTitleCareer {
    margin: 0;
}

.leftTitleCareer {
    font-size: 100px;
    width: 20rem;
}

.right-container {
    display: flex;
    justify-content: end;
    flex-direction: column;
    font-size: 50px;
    text-align: right;
    color: #1e1e1e;
    margin: 20rem 6rem 0 0;

}

.rightFirstName,
.rightLastName {
    margin: 0;
}

@media (min-width: 280px) and (max-width: 767px) {
    .left-container {
        margin: 4rem 2rem;
        font-size: 12px;
    }

    .leftTitleCareer {
        font-size: 45px;
        width: 20rem;
    }

    .right-container {
        font-size: 25px;
        margin: 23rem 2rem 0 0;
    }
}

@media (min-width: 768px) and (max-width: 1024px) {
    .left-container {
        margin: 7rem 4rem;
    }

    .leftTitleCareer {
        font-size: 60px;
        width: 20rem;
    }


    .right-container {
        font-size: 32px;
        margin: 33rem 4rem 0 0;
    }

}

@media (min-width: 1025px) and (max-width: 1280px) {
    .left-container {
        margin: 7rem 6rem;
    }

    .leftTitleCareer {
        font-size: 65px;
        width: 20rem;
    }

    .right-container {
        font-size: 33px;
        margin: 25rem 6rem 0 0;
    }
}

@media (min-width: 1281px) and (max-width: 1899px) {
    .left-container {
        margin: 7rem 6rem;
    }

    .leftTitleCareer {
        font-size: 75px;
        width: 20rem;
    }

    .right-container {
        font-size: 40px;
        margin: 26rem 6rem 0 0;
    }
}
</style>