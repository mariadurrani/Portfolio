<script setup lang="ts">

</script>

<template>
    <div class="copyright">
        <p>&copy; / 2024</p>
    </div>
</template>

<style>
@font-face {
    font-family: "Raleway";
    src: url(../fonts/raleway/Raleway-Regular.ttf);
}

@font-face {
    font-family: "RalewayBold";
    src: url(../fonts/raleway/Raleway-ExtraBold.ttf);
}

.copyright {
    font-family: "Raleway";
    position: fixed;
    font-size: 20px;
}

@media (min-width: 280px) and (max-width: 767px) {
    .copyright {
        
    }
}

@media (min-width: 768px) and (max-width: 1024px) {
    .copyright {
        margin: 0 4rem;
    }
}

@media (min-width: 1025px) and (max-width: 1280px) {
    .copyright {
        margin: 0 6rem;
    }
}

@media (min-width: 1281px) and (max-width: 1899px) {
    .copyright {
        font-size: 20px;
        margin: 0 6rem;
    }

}
</style>
