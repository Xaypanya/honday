<template>
    <header class="sticky top-0 bg-primary shadow-lg">
        <nav class="container flex  flex-row items-center justify-between gap-4 text-white py-3">
            <RouterLink :to="{name: 'home'}">
                <div class="flex items-center gap-1">
                    <!-- <i class="fa-solid fa-cloud-sun text-2xl"></i> -->
                    <img :src="hondayIcon" alt="Honday" class="w-12 -translate-y-1">
                    <p class="text-2xl">Honday </p>
                </div>
            </RouterLink>

            <div class="flex gap-3">
                <i :class="hoverIconStyle" @click="toggleModal" class="fa-solid fa-circle-question text-2xl"></i>
                <i :class="hoverIconStyle" class="fa-solid fa-add text-2xl"></i>
            </div>

            <BaseModal :modalActive="modalActive" @close-modal="toggleModal">
            <div class="text-black">
                <h1 class="text-2xl mb-1 font-bold">About </h1>
                <p class="mb-4">
                    Honday allows you to track the current and future wheather of cities of your choosing.
                </p>
                <h2 class="text-2xl font-bold">How it works </h2>
                <ol class="list-decimal list-inside mb-4">
                    <li>Search for you city by entering the name in search bar</li>
                    <li>Select a city within the results, this will take you to the current wheather of your selection</li>
                    <li>Track the city by clicking on the "+" icon in the top right. This will save the city to view at a later time on the home page.</li>
                </ol>
                <h2 class="text-2xl font-bold">Removing a city </h2>
                <p class="mb-4">
                    If you no longer wish to track a city, simple select the city within the home page, At the bottom of the page, There will be an option to delete the city.
                </p>
            </div>
            </BaseModal>
        </nav>
    </header>
</template>

<script setup>
    import {ref} from "vue"
    import {RouterLink} from "vue-router";
    import {hoverIconStyle} from "../constants/index"
    import hondayIcon from "../assets/images/honday.png"
    import BaseModal from "../components/BaseModal.vue"

    const modalActive = ref(null);

    const toggleModal = () => {
        modalActive.value = !modalActive.value
    }
</script>
