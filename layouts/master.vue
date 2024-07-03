<template>
    <section class="mt-32 w-full grid grid-cols-1 m-auto justify-center content-center">
    <div class="bg-white rounded-tr-3xl mb-10 grid grid-cols-[auto] m-auto container relative rounded-b-3xl">
        <div class="grid grid-cols-[auto_auto] max-mini:grid-cols-1">
            <div class="bg-white max-lg:gap-8 grid-cols-1 grid items-center -mt-20 relative px-8
             w-[52rem] max-minixl:w-[23rem] max-mini:px-2 rounded-tl-3xl max-mini:!w-full max-mini:grid-cols-1fr max-sm:w-fit max-sm:gap-4 max-md:w-[40rem] max-lg:before:hidden max-xl:w-[48rem] before:box-border
            before:bg-no-repeat before:h-full before:content-[''] before:scale-x-[-1]
            max-mini:before:bg-none max-mini:before:w-0 max-mini:before:scale-x-0 
             before:absolute before:bg-contain before:top-0 before:-right-[9.5rem] before:bg-svgTopHead before:w-full">
             <nav class="h-[4rem] mt-6 pt-3 max-mini:h-[4rem] max-mini:pt-0 z-20 rounded-2xl bg-light/70 items-center grid grid-cols-[repeat(4,auto)] webkit-inline-box
             gap-8 max-mini:gap-2 justify-center">
                <NuxtLink :class="{'activeUrl' : $route.name == 'index'}" class="z-10 max-minixl:px-4 max-mini:px-5 max-md:px-6 max-sm:text-xs text-primary-active max-lg:px-8 max-xl:px-6 px-9 h-10 grid items-center text-sm" to="/">About me</NuxtLink>
                <NuxtLink class="z-10 max-minixl:px-4 max-mini:px-5 max-md:px-6 max-sm:text-xs text-primary-active max-lg:px-8 max-xl:px-6 px-9 h-10 grid items-center text-sm" :class="{'activeUrl' : $route.name == 'resume'}" to="/resume">Resume</NuxtLink>
                <NuxtLink class="z-10 max-minixl:px-4 max-mini:px-5 max-md:px-6 max-sm:text-xs text-primary-active max-lg:px-8 max-xl:px-6 px-9 h-10 grid items-center text-sm" :class="{'activeUrl' : $route.name == 'work-samples'}" to="/work-samples">Work samples</NuxtLink>
                <NuxtLink class="z-10 max-minixl:px-4 max-mini:px-5 max-md:px-6 max-sm:text-xs text-primary-active max-lg:px-8 max-xl:px-6 px-9 h-10 grid items-center text-sm" :class="{'activeUrl' : $route.name == 'contact-me'}" to="/contact-me">Contact me</NuxtLink>
            </nav>
        </div>

        </div>
        <div class="grid grid-cols-[26rem_1fr] max-mini:grid-cols-1 max-mini:pt-0 max-lg:grid-cols-1 max-xl:grid-cols-[19rem_1fr] gap-10 max-xl:gap-4 px-6 relative pt-10">
           <Sidebar></Sidebar>
           <slot></slot>
        </div>
    </div>
</section>
</template>

<script setup>

</script>
