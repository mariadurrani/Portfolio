<script setup lang="ts">

</script>

<template>
    <div class="wrapper">
        <nav>
            <a href="#" class="nav">
                <div class="one"></div>
                <div class="two"></div>
                <div class="three"></div>
            </a>
        </nav>


    </div>
</template>

<style>
@font-face {
    font-family: "coolvetica";
    src: url(/Portfolio/src/fonts/coolvetica/coolvetica\ compressed\ hv.otf);
}

.wrapper {
    width: 100%;
    height: 200vh;
    text-align: center;
    font-family: "coolvetica";
    text-transform: uppercase;
}

nav div {
    height: 4px;
    background-color: rgb(0, 0, 0);
    margin: 5px 0;
}

.nav {
    width: 7rem;
    margin: 3rem;
    float: right;
}

.one,
.two,
.three {
    width: 50px;
}
</style>
