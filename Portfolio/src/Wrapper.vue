<script setup lang="ts">
</script>

<template>
  <div class="styled-wrapper">

    <slot></slot>
  </div>
</template>

<style scoped>
.styled-wrapper {
  font-family: "Raleway";
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: 2rem;
}

@media (min-width: 280px) and (max-width: 767px) {
  .styled-wrapper {
    align-items: center;
    margin: 5rem;
  }
}

@media (min-width: 1900px) {
  .styled-wrapper {
    margin: 3rem 8rem 0 8rem;
  }
}

@media (min-width: 768px) and (max-width: 1024px) {}
</style>