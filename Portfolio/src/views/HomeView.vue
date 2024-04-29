<script setup lang="ts">

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

        </main>
    </header>
</template>

<style>
body {
    background-color: #D4ABB2;
}

.home-wrapper {
    font-family: "coolvetica";
    text-transform: uppercase;
}

.left-container {
    display: flex;
    flex-direction: column;
    margin: 8rem 10rem;
}

.leftName,
.leftTitleCareer {
    margin: 0;
}

.leftTitleCareer {
    font-size: 100px;
    width: 100px;
}
</style>