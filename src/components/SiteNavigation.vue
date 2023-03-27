<template>
    <header class="sticky top-0 bg-primary shadow-lg">
        <nav class="container flex  flex-row items-center justify-between gap-4 text-white py-6">
            <RouterLink :to="{name: 'home'}">
                <div class="flex items-center gap-3">
                    <i class="fa-solid fa-cloud-sun text-2xl"></i>
                    <p class="text-2xl">Honday </p>
                </div>
            </RouterLink>

            <div class="flex gap-3"><i :class="hoverIconStyle" class="fa-solid fa-circle-question text-xl"></i></div>
        </nav>
    </header>
</template>

<script setup>
    import {RouterLink} from "vue-router";
    import {hoverIconStyle} from "../constants/index"
</script>
