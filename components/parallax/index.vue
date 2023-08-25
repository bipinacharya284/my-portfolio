<template>
    <div class="relative h-screen overflow-hidden">
        <div class="flex flex-col flex-wrap items-center justify-center mx-10 mt-10 text-center">
            <img src="/img/profile2.jpg" class="rounded-full w-64 h-64 " />
            <span class="text-white text-7xl mt-10">Acharya Bipin</span>
            <span class="text-white text-2xl  mt-5">Undergrad Engineer, Developer</span>
        </div>
        <div class="absolute top-0-0 left-0 w-10/10 h-10/10 -z-10">

            <img src="/img/bg.jpg" alt="Background" class="w-full h-full object-cover fixed top-0 left-0 z-0">

        </div>
        <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2"
            :style="{ transform: `translateY(${offset}px)` }">
            <!-- Your moving content goes here -->
        </div>
    </div>
</template>

<script setup>
defineProps(['offset'])  // This prop will control the vertical movement


</script>

