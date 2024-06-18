<script setup lang="ts">

const projects = [
    { id: 1, label: "Project Name", text: "Year" },
    { id: 2, label: "Project Name", text: "Year" },
    { id: 3, label: "Project Name", text: "Year" }
]
</script>

<template>
    <main class="work-page__wrapper">
        <div class="work-page__text-container">
            <h1 class="work-page__text-container__title">Work</h1>
            <p class="work-page__text-container__desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. In
                adipisci, quia
                ipsa voluptatibus deleniti hic temporibus harum, repudiandae sint, provident error aut ullam nihil
                laboriosam suscipit odio excepturi ratione est.</p>
        </div>

        <div class="work-page__projects-container">
            <ul class="work-page__projects-container__projects">
                <li v-for="project in projects" :key="project.id" className="work-page__project">
                    <span class="work-page__project__project-label">{{ project.label }}</span>
                    <span class="work-page__project__project-text">{{ "-" + " " + project.text }}</span>
                </li>
            </ul>
        </div>
    </main>
</template>

<style src="../assets/WorkView.scss"></style>