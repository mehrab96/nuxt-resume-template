<script setup>

</script>

<template>
    <nav class="h-[4rem] mt-6 pt-3 max-mini:h-[4rem] max-mini:pt-0 z-20 rounded-2xl bg-light/70 items-center grid grid-cols-[repeat(4,auto)] webkit-inline-box
        gap-8 max-mini:gap-2 justify-center">
        <NuxtLink :class="{'activeUrl' : $route.name == 'index'}" class="z-10 max-minixl:px-4 max-mini:px-5 max-md:px-6 max-sm:text-xs text-primary-active max-lg:px-8 max-xl:px-6 px-9 h-10 grid items-center text-sm" to="/">About me</NuxtLink>
        <NuxtLink class="z-10 max-minixl:px-4 max-mini:px-5 max-md:px-6 max-sm:text-xs text-primary-active max-lg:px-8 max-xl:px-6 px-9 h-10 grid items-center text-sm" :class="{'activeUrl' : $route.name == 'resume'}" to="/resume">Resume</NuxtLink>
        <NuxtLink class="z-10 max-minixl:px-4 max-mini:px-5 max-md:px-6 max-sm:text-xs text-primary-active max-lg:px-8 max-xl:px-6 px-9 h-10 grid items-center text-sm" :class="[{'activeUrl' : $route.name == 'work-samples'} , {'activeUrl' : $route.name == 'samples-slug'}]" to="/work-samples">Work samples</NuxtLink>
        <NuxtLink class="z-10 max-minixl:px-4 max-mini:px-5 max-md:px-6 max-sm:text-xs text-primary-active max-lg:px-8 max-xl:px-6 px-9 h-10 grid items-center text-sm" :class="{'activeUrl' : $route.name == 'contact-me'}" to="/contact-me">Contact me</NuxtLink>
    </nav>
</template>